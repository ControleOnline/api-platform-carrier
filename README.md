# carrier


`composer require controleonline/carrier:dev-master`



Create a new fila on controllers:
config\routes\controllers\carrier.yaml

```yaml
controllers:
    resource: ../../vendor/controleonline/carrier/src/Controller/
    type: annotation      
```

Add to entities:
nelsys-api\config\packages\doctrine.yaml
```yaml
doctrine:
    orm:
        mappings:
           carrier:
                is_bundle: false
                type: annotation
                dir: "%kernel.project_dir%/vendor/controleonline/carrier/src/Entity"
                prefix: 'ControleOnline\Entity'
                alias: ControleOnline                             
```          


Add this line on your routes:
config\packages\api_platform.yaml
```yaml          
mapping   :
    paths: ['%kernel.project_dir%/src/Entity','%kernel.project_dir%/src/Resource',"%kernel.project_dir%/vendor/controleonline/carrier/src/Entity"]        
```          
