# Магенто 2-ийн монгол хэлний орчуулга

Магенто 2 дээр орчуулга нэмэх арга өөрчлөгдсөн тул бүх орчуулгыг нэгтгэж 
нэг файл дотор бүх орчуулгыг хийж байгаа. Мэргэжлийн үг хэллэг дээр алдаа
мадаг байвал санал бодлоо илэрхийлэх, эсвэл орчуулах ажилд биечлэн оролцох 
зэргээр нөлөөлж болно.

# Суулгах заавар

Хоёр янзын аргаар суулгаж хэрэглэх боломжтой. 

### Хуулах аргаар суулгах

```
rm pub/static/frontend/Magento/luma/mn_Cyrl_MN/js-translation.json
php bin/magento setup:static-content:deploy mn_Cyrl_MN
php bin/magento setup:upgrade
rm -rf var/di
php bin/magento setup:di:compile
```


### Composer ашиглан суулгах

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


### Орчуулагдсан компонент, модулиуд 

|Орчуулгын файлууд|Орчуулагдсан төлөв|
|---|---|
|Magento_Admin_Notification|100%|
|Magento_Advanced_Pricing_Import_Export|100%|
|Magento_Authorization|100%|
|Magento_Authorizenet|80% орчуулж байгаа|
|Magento_Backend|50% орчуулж байгаа|
|Magento_Backup| |
|Magento_Braintree| |
|Magento_Bundle| |
|Magento_Captcha| |
|Magento_Catalog_Import_Export| |
|Magento_Catalog_Inventory| |
|Magento_Catalog_Rule| |
|Magento_Catalog_Search| |
|Magento_Catalog_Url_Rewrite|100% |
|Magento_Catalog_Widget| |
|Magento_Catalog|100%|
|Magento_Checkout_Agreements| |
|Magento_Checkout|100% |
|Magento_Cms|100% |
|Magento_Config| |
|Magento_Configurable_Product| |
|Magento_Contact|100% |
|Magento_Cookie|100% |
|Magento_Cron| |
|Magento_Currency_Symbol|100% |
|Magento_Customer_Import_Export| |
|Magento_Customer| |
|Magento_Deploy| |
|Magento_Developer|100% |
|Magento_Dhl| |
|Magento_Directory| |
|Magento_Downloadable_Import_Export|100% |
|Magento_Downloadable| |
|Magento_Eav| |
|Magento_Email|100% |
|Magento_Encryption_Key|100% |
|Magento_Fedex| |
|Magento_Gift_Message| |
|Magento_Google_Adwords| |
|Magento_Google_Optimizer|100% |
|Magento_Grouped_Product|100% |
|Magento_Import_Export| |
|Magento_Indexer| |
|Magento_Integration| |
|Magento_Layered_Navigation|100%|
|Magento_Marketplace| |
|Magento_Media_Storage| |
|Magento_Msrp|100% |
|Magento_Multishipping| |
|Magento_New_Relic_Reporting| |
|Magento_Newsletter| |
|Magento_Offline_Payments| |
|Magento_Offline_Shipping| |
|Magento_Page_Cache| |
|Magento_Payment| |
|Magento_Paypal| |
|Magento_Persistent| |
|Magento_Product_Alert| |
|Magento_Product_Video| |
|Magento_Quote|100%|
|Magento_Reports| |
|Magento_Review|100%|
|Magento_Rss|100% |
|Magento_Rule|100% |
|Magento_Sales_Rule||
|Magento_Sales_Sequence| |
|Magento_Sales|100%|
|Magento_Search|100%|
|Magento_Send_Friend| |
|Magento_Shipping| |
|Magento_Sitemap| |
|Magento_Store|100%|
|Magento_Swatches| |
|Magento_Tax_Import_Export|100% |
|Magento_Tax| |
|Magento_Theme| |
|Magento_Translation|100%|
|Magento_Ui| |
|Magento_Ups| |
|Magento_Url_Rewrite| |
|Magento_User| |
|Magento_Usps| |
|Magento_Variable|100%|
|Magento_Webapi| |
|Magento_Weee| |
|Magento_Widget| |
|Magento_Wishlist|100% Ganzorig|
|lib/web/mage/adminhtml/backup.js|100%|
|lib/web/mage/adminhtml/wysiwyg/widget.js|100%|
|lib/web/mage/backend/suggest.js|100%|
|lib/web/mage/decorate.js|100%|
|lib/web/mage/dropdown.js|100%|
|lib/web/mage/loader.js|100%|
|lib/web/mage/loaderold.js|100%|
|lib/web/mage/menu.js|100%|
|lib/web/mage/translate-inline-vde.js|100%|
|lib/web/mage/translate-inline.js|100%|
|lib/web/mage/validation.js|100%|
|lib/web/mage/validation/validation.js|100%|
|Magento_Google_Analytics| |
|Magento_Webapi_Security| |
|frontend/magento/blank|100%|
|frontend/magento/luma|100%|
