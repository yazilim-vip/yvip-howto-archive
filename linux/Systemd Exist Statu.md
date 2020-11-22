Systemd Exist Status

Bir servis işlemi sonlandırıldığı zaman bir kod döndürüyor. Systemd normal şartlar altında başırılı sonuç olarak 100 değerini bekliyor. 
Ancak Java uygulamaları başarılı bir şekilde  sonlandırıldığında exit code 143 olarak belirlenmiş. Biz java process durduruyoruz.
Eğer servise bunu belirtmesek servisi durduduuğmuzda dönüş kodu 143 oluyor ancak systemd bunu failed olarak görüyor. Bu sebeple servis fail olmuş olarak gösteriliyor.
Bu durumun önüne geçmek için  SuccessExitStatus=143 satırı eklenerek, servisin başarılı bir şekilde durduğunu anlaaası için bakması gereken kodun 143 olduğunu  nalıyor.

Gerekli systemd ayar dosyası
------------------------------------------------------------------------------------------

[Unit]
Description=OctoServer Alarm Service
After=syslog.target
# StartLimitIntervalSec in recent systemd versions
StartLimitInterval=0

[Service]
SuccessExitStatus=143
WorkingDirectory=/folder/to/jar_file
SyslogIdentifier=MyAwesomeJavaApp
ExecStart=/usr/bin/java -jar /path/to/jar_file

User=user_runs_java_app
Type=simple
Restart=always
# time to sleep before restarting a service
RestartSec=1

[Install]
WantedBy=multi-user.target