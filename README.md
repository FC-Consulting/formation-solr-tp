# Formation Solr TP

## But

![img.png](img.png)

Nous allons ajouter des données dans une base MariaDB via une application (write).
Au travers d'un DataImportHandler, Solr va indexer, selon une requête définit, 
ces données. Et nous pourrons les restituer au travers du moteur de recherche.  

## Pour commencer

### Cloner le projet

```git
git clone https://github.com/FC-Consulting/formation-solr-tp.git
cd formation-solr-tp
```

### Solr 

```shell
sudo nano /etc/security/limits.conf

solr hard nofile 65535
solr soft nofile 65535
solr hard nproc 65535
solr soft nproc 65535

apt-get install haveged -y
```

## Etape 2 :: Vérification 

```shell
./gradlew run
```

```shell
> Task :app:run
Hello World!

BUILD SUCCESSFUL in 992ms
2 actionable tasks: 2 executed
```

## Etape 3 :: Ajout des dépendances

```groovy
dependencies {
    ...
    implementation 'org.apache.camel:camel-solr:2.9'
}
```

## Etape 4 :: 
