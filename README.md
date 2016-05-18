# Магенто 2-ийн монгол хэлний орчуулга

Магенто 2 дээр орчуулга нэмэх арга өөрчлөгдсөн тул бүх орчуулгыг нэгтгэж 
нэг файл дотор бүх орчуулгыг хийж байгаа. Мэргэжлийн үг хэллэг дээр алдаа
мадаг байвал санал бодлоо илэрхийлэх, эсвэл орчуулах ажилд биечлэн оролцох 
зэргээр нөлөөлж болно.

# Суулгах заавар

Хоёр янзын аргаар суулгаж хэрэглэх боломжтой. 

1. Хуулах аргаар суулгах

```
rm pub/static/frontend/Magento/luma/mn_Cyrl_MN/js-translation.json
php bin/magento setup:static-content:deploy mn_Cyrl_MN
php bin/magento setup:upgrade
rm -rf var/di
php bin/magento setup:di:compile
```


2. Composer ашиглан суулгах

Composer.json файлын "repositories" блок дотор нэмнэ:   

```
    {
        "type": "vcs",
        "url": "https://ulzii@bitbucket.org/ulziit/magento2_mongolian_localepack_mn_cyrl_mn.git"
    }
```   
 
мөн энэ мөрийг "require" блок дотор нэмнэ

``` 
"ulzii/mage2-locale-mn-cyrl-mn": "dev-master"
```


```
composer update
rm pub/static/frontend/Magento/luma/mn_Cyrl_MN/js-translation.json
php bin/magento setup:static-content:deploy mn_Cyrl_MN
```


Үүний дараа магенто удирдлагын хэсэгт системийн хэлийг "Mongolian" сонгоод хадгална. Кэйчээ хоослохоо мартаж бас болохгүй шүү.

