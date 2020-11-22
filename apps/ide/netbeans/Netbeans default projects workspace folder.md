Netbeans default projects workspace folder

How to change the default project directory (folder) in Netbeans


I don't think you can make it module-specific but you can set it as follows:

1. Close NetBeans
2. Find the projectui.properties file. For me (Windows) it was under C:\Documents and Settings\Catchwa\.netbeans\6.9\config\Preferences\org\netbeans\modules\projectui.properties
3. The projectsFolder=C:\\NetBeansProjects variable is I think what you want to change.



[stackoverflow_link](https://stackoverflow.com/a/3082720)

**NOT**: Linux için dizin: *$HOME/.netbeans/$VERSION/config/Preferences/org/netbeans/modules where $VERSION*