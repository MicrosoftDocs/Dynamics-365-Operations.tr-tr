---
title: İşlem yapılacak yerleşimler oluşturma
description: Bu makalede Varlık Yönetimi'nde işlem yapılacak yerleşimler oluşturma işlemi açıklanmaktadır.
author: johanhoffmann
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationCopyStructure, EntAssetFunctionalLocationCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 503150e7cfc580821c5ed8d4c4c9b56998f6ff13
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869734"
---
# <a name="create-functional-locations"></a>İşlem yapılacak yerleşimler oluşturma

[!include [banner](../../includes/banner.md)]

 

Bu makalede Varlık Yönetimi'nde işlem yapılacak yerleşimler oluşturma işlemi açıklanmaktadır.

İşlem yapılacak yerleşim yapısı oluşturduğunuzda, işlem yapılacak bir yerleşim oluşturduktan sonra bunu özgün konumdan taşıyamazsınız. Bu, Varlık Yönetiminde oluşturmaya başlamadan önce işlem yapılacak yerleşimlerin yapısını dikkatle değerlendirmeniz gerektiği anlamına gelir. İşlem yapılacak bir yerleşimden memnun değilseniz, henüz kullanıma alınmamış olması durumunda bunu silebilirsiniz.

İşlem yapılacak yerleşimlerle çalışabilmek için işlem yapılacak yerleşimler için iki "kategori" oluşturarak başlayabilirsiniz:

- Alt yerleşimleri bulunmayan *bir* varsayılan işlem yapılacak yerleşim oluşturun. Bu işlem yapılacak yerleşim, yeni varlıklar oluşturduğunuzda varlıklar için yalnızca standart yerleşim olarak kullanılır.  
- Şirketinizdeki bakım işlerini yönetmek için gereken işlem yapılacak yerleşim yapılarını oluşturun.

## <a name="create-a-default-functional-location"></a>Varsayılan işlem yapılacak yerleşim oluşturma

İşlem yapılacak yerleşimleri kullandığınızda, yeni varlıklar oluştururken kullanılacak bir varsayılan işlem yapılacak yerleşim oluşturarak başlayın. Bu işlem yapılacak yerleşim **Varlık yönetimi** > **Kurulum** > **Varlık yönetimi parametreleri** > **Varlıklar** bağlantısı > **Varsayılan işlem yapılacak yerleşim** alanında seçtiğiniz konumdur. Varsayılan işlem yapılacak yerleşim yeni varlıklar oluştururken bu varlıklar için işlem yapılacak yerleşim yapısı oluşturmadığınızda kullanılabilir.

1. **Varlık yönetimi** > **Genel** > **İşlem yapılacak yerleşimler** > **Tüm İşlem yapılacak yerleşimler**'i seçin.  
2. **Tüm işlem yapılacak yerleşimler**'de **Yeni**'yi seçin.
3. **İşlem yapılacak yerleşim** alanına bunun özel bir işlem yapılacak yerleşim olduğunu belirtmek için "0000" veya "Varsayılan" gibi bir kimlik ekleyin.
4. **Ad** alanına varsayılan işlem yapılacak yerleşim için bir ad girin.
5. **Üst** alanında herhangi bir üst öğe *seçmeyin* – bu alanı boş bırakın.
6. **İşlem yapılacak yerleşim türü** alanında, varsayılan işlem yapılacak yerleşim için kullanılacak işlem yapılacak yerleşim türünü seçin. İşlem yapılacak yerleşim türlerini ayarlamayla ilgili dah afazla bilgi için bkz. [İşlem yapılacak yerleşim türleri](../setup-for-functional-locations/functional-location-types.md).
7. **Tamam**'ı seçin. Şirketiniz tarafından kullanılan işlem yapılacak yerleşimlere varlıkları yükleyinceye kadar yalnızca yeni varlıklar için geçici bir konum olarak kullanıldığından, bu işlem yapılacak yerleşime daha fazla veri eklemeyin.

## <a name="create-functional-locations"></a>İşlem yapılacak yerleşimler oluşturma

Aşağıdaki yordamda, şirketinizdeki bakım yönetimi için gerekli işlem yapılacak yerleşimleri nasıl oluşturacağınız açıklanmaktadır.

1. **Varlık yönetimi** > **Genel** > **İşlem yapılacak yerleşimler** > **Tüm İşlem yapılacak yerleşimler**'i seçin. Kılavuz görünümü veya ayrıntılar görünümünden işlem yapılacak yerleşim oluşturabilirsiniz.
2. **Yeni** düğmesini seçin.
3. **İşlem yapılacak yerleşim** alanına bir kimlik ekleyin.
4. **Ad** alanına işlem yapılacak yerleşim için bir ad girin.
5. İşlem yapılacak yerleşim bir yapıdaki bir alt konumsa, **Üst** alanda üst konumu seçin.
6. **İşlem yapılacak yerleşim türü** alanında türü seçin.
7. **Tamam**'ı seçin.
8. İşlem yapılacak yerleşimi seçin ve daha fazla bilgi eklemek için **Düzenle** düğmesine tıklayın.

>[!NOTE]
>İşlem yapılacak yerleşim yaşam döngüsü durumları kurulumunuza bağlı olarak, işlem yapılacak yerleşim için tüm alt konumları oluşturmanız ve sonra varlıkları yüklemeye başlamadan önce işlem yapılacak yerleşim yaşam döngüsü durumunu değiştirmeniz gerekebilir. Varlık yükleme hakkında daha fazla bilgi için bkz. [Varlıkları işlem yapılacak yerleşimlere yükleme](../functional-locations/install-objects-on-functional-locations.md). İşlem yapılacak yerleşim yaşam döngüsü durumları kurulumu hakkında daha fazla bilgi için bkz. [İşlem yapılacak yerleşim yaşam döngüsü durumları](../setup-for-functional-locations/functional-location-stages.md).

Ayrıntılar görünümünde, işlem yapılacak yerleşim hakkında bilgi ekleyebileceğiniz ve düzenleyebileceğiniz hızlı sekmeleri görürsünüz.

## <a name="general-information"></a>Genel Bilgiler

Bu bölüm, işlem yapılacak yerleşim yapısındaki üst ve alt bilgilerine genel bir bakış sağlar. **Ayrıntılar** bölümünde, işlem yapılacak yerleşimle ilgili çok sayıda varlık özniteliği, bakım planı ve varlık görebilirsiniz. **Stok** bölümünde, işlem yapılacak yerleşimin ilişkili olduğu tesisi ve ambarı seçebilirsiniz. Tesis ve ambar iş emri madde tahminleriyle bağlantılı olarak kullanılır. Madde tahmini oluştururken, varlığın işlem yapılacak yerleşiminden alınan tesis ve ambar bilgileri otomatik olarak kullanılır. **Yaşam döngüsü durumu** bölümünde, işlem yapılacak yerleşim yaşam döngüsü durumu hakkında bilgi görüntülenir.

## <a name="installed-assets"></a>Yüklü varlıklar

Varlık yükleme hakkında daha fazla bilgi için bkz. [Varlıkları işlem yapılacak yerleşimlere yükleme](../functional-locations/install-objects-on-functional-locations.md). Bu hızlı sekmedeki **Görüntüle** düğmesini hızlı sekmedeki daha fazla alanı görüntülemek için kullanabilirsiniz. **Geçerlilik başlangıcı** ve **Alt varlık** alanları kılavuzda gösterilebilir.

## <a name="asset-attribute-requirements"></a>Varlık öznitelik gereksinimleri

Bu hızlı sekmede, işlem yapılacak yerleşime yüklediğiniz varlıklar için belirli öznitelik gereksinimleri ekleyebilirsiniz. Bu gereksinimler yalnızca bilgi amaçlıdır. Başka öznitelik gereksinimleri bulunan varlıkları yüklemenizi engellemez. **Satır ekle**'yi ve öznitelik türünü seçin. Sonra ilgili **Değeri** ekleyin, **Eşik ölçütü** alanında bir eşik seçin ve kaydı kaydedin.

## <a name="maintenance-plans-and-maintenance-rounds"></a>Bakım planları ve Bakım sıraları

Burada, başlangıç tarihi de dahil olmak üzere işlem yapılacak yerleşime bakım planları ve bakım sıraları ekleyebilirsiniz. İşlem yapılacak yerleşime yüklü varlıkların ayarlanmış başka bakım planları olabilir. Tüm bakım planları ve bakım sıraları, işlem yapılacak yerleşim ve yüklenmiş varlıklar için varlık takvimi girişlerini planlamak amacıyla kullanılabilir.

>[!NOTE]
>Bakım planlarını zamanladıktan sonra **Tüm işlem yapılacak yerleşim** ayrıntılı görünümü > **Bakım planları** hızlı sekmesindeki bakım planlarında varlık türleri, varlık markaları ve varlık modelleri ayarını güncelleştirirseniz, bu işlem yapılacak yerleşimle ilgili mevcut bakım zamanlaması girişleri otomatik olarak silinir. İşlem yapılacak yerleşimdeki güncelleştirilmiş bakım planı ayarına karşılık gelen yeni zamanlama girişleri oluşturmak için, bu işlem yapılacak yerleşim için yeni bir bakım planı zamanlaması çalıştırmanız gerekir. 

## <a name="address"></a>Adres

**Adres** hızlı sekmesine işlem yapılacak yerleşim adresini ekleyin. İşlem yapılacak yerleşimlerdeki adresler devralınır, yani bir alt konumun tanımlanmış adresi yoksa, üst konumun adresi kullanılır.

## <a name="workers"></a>Çalışanlar

Bu hızlı sekmede, işlem yapılacak yerleşime bağlı çalışanlar ekleyebilir ve çalışan için birincil olarak işlem yapılacak yerleşim seçebilirsiniz. 

## <a name="attributes"></a>Öznitelikler

Bu hızlı sekmede, işlem yapılacak yerleşim öznitelikleri için değerler ayarlayabilirsiniz. Bu öznitelikler, işlem yapılacak yerleşimle ilgili yapısal özellikler, yapı türü, alan açıklamaları veya zemin üstündeki veya altındaki yerleşim gibi özellikleri veya teknik özellikleri açıklamak için kullanılabilir.

**Satır ekle**'yi ve öznitelik türünü seçin. Ardından, öznitelik türü ile ilgili **Değeri** ekleyin ve kaydı kaydedin.

## <a name="financial-dimensions"></a>Mali boyutlar

İşlem yapılacak yerleşim için mali boyutları seçebilirsiniz. [İşlem yapılacak yerleşim türleri](../setup-for-functional-locations/functional-location-types.md), mali boyutların işlem yapılacak yerleşimden otomatik güncelleştirilmesine izin verecek şekilde ayarlanabilir. Bu, bir mali boyuta yüklenen varlıkların otomatik olarak işlem yapılacak yerleşime ilişkin mali boyutları alacağı gelir. Bu, konumlara bağlı olarak farklı maliyet merkezleri istiyorsanız yararlıdır.

**Tesis**, **Ambar**, **Adres** ve **Mali boyutlar** ile ilgili veriler bir üst işlem yapılacak yerleşimde güncelleştirildiğinde, güncelleştirme sırasında seçim yaparsanız ilgili alt işlem yapılacak yerleşimler buna göre güncelleştirilebilir. Güncelleştirme seçeneklerini sunan bir iletişim kutusu açılır.

## <a name="copy-a-functional-location-structure"></a>İşlem yapılacak yerleşim yapısını kopyalama

Şirketinizin benzer konum yapılarına sahip çeşitli İşlem yapılacak yerleşimleri varsa, hızlı bir şekilde bir dizi benzer konum hiyerarşileri oluşturmak için Varlık Yönetimi'ndeki kopyalama işlevini kullanabilirsiniz. Belirli bir İşlem yapılacak yerleşimi veya tüm yapıyı kopyaladığınızda, yeni konum veya yapı, kopyaladığınızla aynı adı taşır. Kopyalama yordamı gerçekleştirildikten sonra, yeni işlem yapılacak yerleşim için seçilen işlem yapılacak yerleşim yaşam döngüsü durumu izin verdiği taktirde, yeni işlem yapılacak yerleşimdeki adı veya diğer ayarları kolayca değiştirebilirsiniz.

1. **Tüm işlem yapılacak yerleşimler**'de, kopyalamak istediğiniz işlem yapılacak yerleşimi seçin. Örneğin, alt konumlar da dahil olmak üzere tüm işlem yapılacak yerleşim yapısını kopyalamak istiyorsanız, bir üst konum (üst) seçin.
2. **işlem yapılacak yerleşim yapısını kopyala** düğmesini seçin. Liste sayfasında seçtiğiniz konum, **Kopyalama kaynağı** alanında gösterilir.
3. Yeni konumun adını **Yeni işlem yapılacak yerleşim** alanına ekleyin.
4. **Altına yapıştırılacak üst öğe** alanında, oluşturduğunuz konumun mevcut bir işlem yapılacak yerleşim yapısının parçası olması gerekiyorsa, yalnızca bir üst kimliği eklemeniz gerekir.
5. **Tamam**'a tıklayın. Yeni işlem yapılacak yerleşim yapısı **Tüm işlem yapılacak yerleşimler**'de gösterilir.

>[!NOTE]
>İşlem yapılacak yerleşim yapısını kopyaladığınızda, yeni yapıdaki işlem yapılacak yerleşim yaşam döngüsü durumları, işlem yapılacak yerleşim için oluşturduğunuz "ilk duruma" ayarlanır. **Tüm işlem yapıalcak yerleşimler**'deki **Yeniden adlandır** ve **Sil** düğmelerini kullanarak bir işlem yapılacak yerleşimi yeniden adlandırma veya silme, işlem yapılacak yerleşimin geçerli yaşam döngüsü durumuna bağlıdır.

## <a name="delete-a-functional-location"></a>İşlem Yapılacak Yerleşimi Silme

Silmeye çalıştığınız herhangi bir işlem yapılacak yerleşimde yüklü varlık yoksa ve geçerli işlem yapılacak yerleşim yaşam döngüsü durumu izin veriyorsa ilgili alt konumları bulunan bir işlem yapılacak yerleşim silinebilir.

1. **Tüm işlem yapılacak yerleşimler**'de, silmek istediğiniz işlem yapılacak yerleşimi seçin.
2. Gerekirse, işlem yapılacak yerleşimi, işlem yapılacak yerleşimin silinmesine izin veren bir işlem yapılacak yerleşim yaşa döngüsü durumuyla güncelleştirin.
3. **Sil**'i seçin.

>[!NOTE]
>İşlem yapılacak yerleşimi silemezsiniz, silme işlemini bu amaca yönelik bir işlem yapılacak yerleşim yaşam döngüsü durumu ayarlayarak yapabilirsiniz. Örneğin, **İşlem yapılacak yerleşim yaşam döngüsü durumları** formunda, etkin bir aşama olmaması gereken bir "Iskartaya çıkarıldı" veya "Silindi" aşaması ayarlayabilirsiniz.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]