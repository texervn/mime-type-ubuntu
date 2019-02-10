# mime-type-ubuntu
Change the mime-type icon for djvu

1) Copy [i]image-vnd-djvu.svg[/i] to [i]/usr/share/icons/gnome/scalable/mimetypes[/i]

2) Update the icon-cache:
                        sudo update-icon-caches /usr/share/icons/gnome/ -f

3) Edit freedesktop.org.xml:
                            sudo nano /usr/share/mime/packages/freedesktop.org.xml

                            change the following information:
                            <mime-type type="image/vnd.djvu">:
                            +<generic-icon name="image-vnd-djvu"/>
                            
                            <mime-type type="image/vnd.djvu+multipage">:
                            -<generic-icon name="x-office-document"/>
                            +<generic-icon name="image-vnd-djvu"/>
                            
4) Update mime database:
                       sudo update-mime-database /usr/share/mime
