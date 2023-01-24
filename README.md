## Compile Storefront Components in Shopware 6
```bash
docker machine > bin/console plugin:refresh
docker machine > bin/console plugin:install PLUGINNAME
docker machine > bin/console plugin:activate PLUGINNAME

docker machine > copy changed StorefrontJS files to machine
docker machine > ./bin/build-storefront.sh

remote server  > copy compiled minified StorefrontJS to server
location       > plugindir/src/Resources/app/storefront/dist/storefront/js/full-plugin-name.js

remote server  > bin/console theme:compile
remote server  > bin/console cache:clear
```
