---
title: "Ambar yapılandırma şablonu kullanarak bir ambarı ayarlama"
description: "Bu konu ambar yapılandırma şablonu kullanarak bir ambarın nasıl ayarlanacağını açıklamaktadır."
author: perlynne
manager: AnnBe
ms.date: 11/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DataManagementWorkspace, DMFQuickImportExportEnhanced, DMFDefinitionGroupTemplate, DMFEntityTemplateDefinitionLoadDialog
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: AX 7.3
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: 87ade03ec2ba78c4d7f5832bfa6dc1b7eabd8d94
ms.contentlocale: tr-tr
ms.lasthandoff: 12/14/2017

---

# <a name="set-up-a-warehouse-by-using-a-warehouse-configuration-template"></a>Ambar yapılandırma şablonu kullanarak bir ambarı ayarlama

[!include[banner](../includes/banner.md)]

Bu konu ambar yapılandırma şablonu kullanarak bir ambarın nasıl ayarlanacağını açıklamaktadır. Kullanabileceğiniz çeşitli önceden tanımlanmış yapılandırma şablonları bulunur. Bu şablonların nasıl kullanılacağı hakkında bilgi için bkz. [Yapılandırma veri şablonları](../../dev-itpro/data-entities/configuration-data-templates.md).

## <a name="scenarios-where-configuration-templates-can-be-helpful"></a>Yapılandırma şablonlarının yardımcı olabileceği senaryolar

Yapılandırma şablonları bir çok senaryoda yararlı olabilir. Burada bazı örnekler verilmiştir:

- Test ortamında bir yapılandırma ayarını tamamlayıp test ettiniz ve şimdi ayarı üretim ortamına kopyalamak istiyorsunuz.
- Ambar ayarını çeşitli tüzel kişiliklere yaymak veya aynı tüzel kişilikte yeni bir ambar oluşturmak istiyorsunuz.
- Ambar işlevi için hızlı bir şekilde bir demo hazırlamak istiyorsunuz.
- Mevcut maddelerin ve depoların Stok yönetimi yerine Ambar yönetimindeki işlevi kullanmasını istiyorsunuz.

Bu konu bu senaryoların ilkine odaklanır. Bir yapılandırma ayarını test ortamından üretim ortamına kopyalamak için bir yapılandırma şablonunu nasıl kullanabileceğinizi gösterir.

## <a name="copy-a-configuration-setup-from-a-test-environment-to-a-production-environment"></a>Bir yapılandırma ayarını test ortamından üretim ortamına kopyalama

Bu senaryoda, ambar yapılandırma ayarı ve bazı hareket süreçleri zaten test ortamında bulunmaktadır. Şimdi ambar yapılandırma ayarını test ortamından üretim ortamına kopyalamak istiyorsunuz.

> [!NOTE]
> Bir yapılandırma ayarını kopyalarken diğer ilgili ayar verilerini de eklemeniz önemlidir. Örneğin, ayarı test ortamından kopyalayarak ürünler ayarlamak istediğinizi varsayalım. Bununla birlikte, ürün oluşturulmadan önce ürün için sabit çekme konumu ayarlayamazsınız. Tek tek yapılandırma şablonları bu tür bir bağımlılığı desteklememesine karşın, bunu destekleyen varsayılan veri şablonları bulunur. Bu varsayılan veri şablonlarını yapılandırma sürecine kolaylıkla dahil edebilirsiniz.

### <a name="export-a-default-warehouse-template"></a>Varsayılan ambar şablonunu dışa aktarma 

1. **Veri yönetimi** çalışma alanını açın.

    > [!NOTE]
    > Bu çalışma alanını ilk kez kullanıyorsanız, devam etmeden önce tüm veri varlıklarını yüklemeniz gerekir

2. **Şablonlar** kutusunu seçin ve varsayılan şablonları yüklemek için **Varsayılan şablonları yükle**'yi seçin.

    > [!NOTE]
    > **Varsayılan şablonları yükle** yalnızca **Gelişmiş** görünümde kullanılabilir. **Çerçeve parametreleri**'ni ve daha sonra **Varsayılanları görüntüle** alanında **Gelişmiş görünümü** seçin.

3. Varsayılan şablonlar yüklendikten sonra, iş gereksinimlerinizi karşılayacak şekilde bunları değiştirebilirsiniz.

    > [!NOTE]
    > Varsayılan şablonları yüklemek ve şablonları içe aktarmak için sistem yöneticisi erişiminiz olmalıdır. Bu gereksinim tüm varlıkların şablona doğru şekilde yüklenmesini sağlamaya yardımcı olur.

4. Şirkete özel verileri dışa aktarmak istediğiniz tüzel kişilikte olduğunuzdan emin olun.
5. Çalışma alanında **Dışa aktar**'ı seçin.
6. Yeni bir dışa aktarma projesi oluşturun.
7. **+ Şablon ekle**'yi seçin ve **400 - WMS** varsayılan ambar şablonunu bulun. Bu şablon ambar yapılandırması için veri varlıkları ekler.

    > [!NOTE]
    > Dışa aktardığınız verilerin filtrelenmesi gerekirse (örneğin, yalnızca belirli bir ambarla ilgili verileri dışa aktarma istiyorsanız), her veri varlığını değerlendirmeniz ve sorgu aracılığıyla filtre eklemeniz gerekir. Alternatif olarak, tüm verileri dışa aktarabilir ve ardından hedef dosyalarda istenmeyen kayıtları silebilirsiniz.

8. **Dışa Aktar**'ı seçin. Projedeki tüm veri varlıklarıyla ilişkili veriler dışa aktarılır.

Veri paketi için bir zip dosyası indirebilirsiniz. Bu dosya tüm verileri seçilen biçimde (örneğin, Excel biçiminde) içerir. Belirtildiği gibi veri paketi dosyalarındaki bazı kayıtların bunları üretim ortamına aktarmadan önce güncelleştirilmesi gerekebilir. Bir kaydı güncelleştirirseniz, dosya adını değiştirmediğinizden emin olun.

### <a name="import-a-warehouse-configuration-setup"></a>Bir ambar yapılandırması ayarını içe aktarma

1. Hedef ortamda, ambar verilerini içe aktarmak istediğiniz şirkette olduğunuzdan emin olun.

    > [!NOTE]
    > İçe aktarma işlemini yapmadan önce tüm veri bağımlılıklarını tanımlamanız gerekir. Örneğin, **Ambar yönetimi** şablonu **Ambar değerlendirme kodları** adında bir veri varlığı içerir. Bu varlık, **Değerlendirme kodları** ayar sayfasıyla ilişkili verileri içerir (**Ambar yönetimi** > **Kurulum** > **Mobil cihaz** > **Değerlendirme kodları**). Mevcut bir ayar satış siparişleri için iade sürecini zaten işliyorsa, **İade değerlendirme kodu** alanında bir değer bulunur. Bu alandaki değerlendirme kodu **Satış ve pazarlama** şablonunun bir parçası olan **Değerlendirme kodu** veri varlığıyla ilişkilidir. **Değerlendirme kodu** veri varlığındaki veriler **Ambar değerlendirme kodları** alanındaki verilerden önce içe aktarılmazsa, içe aktarma işlemi başarısız olur.

2. **Veri yönetimi** çalışma alanında **İçe aktar**'ı seçin.
3. Yeni bir içe aktarma projesi oluşturun.
4. **+ Dosya ekle**'yi seçin ve veri paketi zip dosyasını yükleyin.
5. **İçe aktar**'ı seçin. **Gelişmiş** görünümde, içe aktarma sırasında oluşabilecek sorunların genel bir görünümünü almak için **Filtre** seçeneğini kullanabilirsiniz.

**Yürütmeyi görüntüle** günlüğü içe aktarılan her veri varlığıyla ilgili ayrıntılı bilgi sağlar. Hedef verilere hızlıca gitmek için aşamalandırma verisi görünümünü kullanabilirsiniz. Bu şekilde, uygulamadaki ilgili sayfalarda içe aktarılan verilen nasıl göründüğünü görebilirsiniz. Varsayılan veri şablonlarını kullandığınızda, her veri varlığı için içe aktarma sırası önceden tanımlanan şekilde çalışarak tüm bağımlı verilerin önce içe aktarılmasını sağlamaya yardımcı olur. Özel veri varlıkları projesinin bir parçasıysa, doğru sıranın tanımlandığından emin olmanız gerekir. Daha fazla bilgi için bkz. [Yapılandırma veri şablonları](../../dev-itpro/data-entities/configuration-data-templates.md).

## <a name="related-topic"></a>İlgili konu

[Konfigürasyon verisi şablonları](../../dev-itpro/data-entities/configuration-data-templates.md)

