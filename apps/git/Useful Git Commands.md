# Useful Git  commands

* Git comitlerinin compakt birformatta konsol üzerinde gösterilmesi
    ```bash
    $ git log --pretty=oneline
    ```
* Gün içerisinde yapılmış tüm commit'leri listelemek
    ```bash
    $ git log --pretty=oneline --since=today.00:00am
    ```
* Gün içinde saat Sabah 08:30'dan sonra yapılmış commitler'in listelenmesi
    ```bash
    $ git log --pretty=oneline --since=today.08:30am
    ```


https://www.mobilhanem.com/git-egitimi/