---
title: Ambar yapılandırması ile ilgili sorunları giderme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ı yapılandırırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1dbd947f0740d22e0f79e6d5c272beb64715c8a5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814404"
---
# <a name="troubleshoot-warehouse-configuration"></a>Ambar yapılandırması ile ilgili sorunları giderme

[!include [banner](../includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ı yapılandırırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a>Şu hata iletisini alıyorum: "Plaka veya konum geçerli değil."

### <a name="issue-description"></a>Sorun açıklaması

Bu hata iletisini, bir plaka kimliğini veya konumu taradığınızda alırsınız.

### <a name="issue-resolution"></a>Sorunun çözümü

Plaka kimliğinin başka bir şey tarafından ayrılmadığından emin olun. Bu sorun, bir kullanıcının Ambar Yönetimi mobil uygulamasında taradığı değer, hem geçerli bir konum hem de geçerli bir plaka olduğunda oluşurdu. Ancak, bu sorun 10.0.11 sürümünde giderilmiştir.

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a>Şu hata iletisini alıyorum: "Bu konum için plaka belirtilmelidir."

### <a name="issue-description"></a>Sorun açıklaması

Bu hata iletisini, gelişmiş ambar yönetimi (WMS) için etkinleştirilen bir ambarı kullanarak transfer emri oluşturup ardından iş tamamlandıktan sonra sevkiyatı onaylamaya çalışırsanız alırsınız.

### <a name="issue-resolution"></a>Sorunun çözümü

**Varsayılan giriş konumu** alanı, "çıkış" ambarına ait bir transit ambar için boştur. Bu sorunu gidermek için transit ambarında varsayılan bir giriş konumu belirtin. Bu konumun plaka denetimli olduğundan emin olun.

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a>Şu hata iletisini alıyorum: "İş türü geçerli olmadığından, Stok durumu değişikliği için iş şablonu satırı oluşturamazsınız. Farklı bir iş türü seçin."

### <a name="issue-description"></a>Sorun açıklaması

Bir çalışma şablonu için, **Çalışma şablonu ayrıntıları** bölümünün **İş türü** sütunundan *Stok durumu değişikliği*'ni seçemezsiniz.

### <a name="issue-resolution"></a>Sorunun çözümü

Bu davranış tasarımdan kaynaklanır. *Stok durumu değişikliği* iş türü, yalnızca sistem süreçleri tarafından kullanılır. Bu değer yapılandırılamaz. İş türleri listesi bir numaralandırma olarak düzeltildiğinden, ekstra girişler, **İş türü** açılan menüsünden filtre dışı bırakılamaz.

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a>Şu hata iletisini alıyorum: "Miktar 1% birimi için geçerli değil."

### <a name="issue-description"></a>Sorun açıklaması

Tek bir konumda birden fazla plakası olan malzeme çekme işi varken miktar *ea* birimi için geçerli değildir.

### <a name="issue-resolution"></a>Sorunun çözümü

Serbest bırakılan ürün veya ürün varyantındaki **Birim dizisi grup kodu** ve **Birim dönüştürmeleri** alanlarının doğru ayarlandığını doğrulayın.

Hata iletisinin sürüm 10.0.15'te geliştirilmiş olduğunu (bkz. [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)) unutmayın. Yeni hata iletisi şöyledir: "Miktar geçerli değil. Beklenen %1 %2."

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>Satış siparişi yerine koyma işinin konum yönergelerinde, çoklu SKU seçeneği birden çok konum yönergesi eylemini değerlendirmez.

### <a name="issue-description"></a>Sorun açıklaması

*Satış siparişleri* iş emri türünün konum yönergeleri ve *Yerine koyma* iş türü, **Birden Fazla SKU** seçeneği seçiliyken, çoklu konum yönergesi eylemlerini değerlendirmez. Yalnızca ilk konum yönergesi eylemi değerlendirilir.

### <a name="issue-resolution"></a>Sorunun çözümü

10.0.15 sürümüne *Çoklu SKU konum yönergeleri için tüm eylemleri değerlendir* adlı yeni bir özellik eklendi (bkz. [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Bu özellik çoklu SKU konum yönergeleri için tüm eylemleri değerlendirir. Bu özelliğe gereksinim duyarsanız, etkinleştirmek için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ni kullanın.

## <a name="i-cant-use-the-warehouse-management-mobile-app-to-do-partial-picking"></a>Kısmi malzeme çekme yapmak için Ambar Yönetimi mobil uygulamasını kullanamıyorum.

### <a name="issue-description"></a>Sorun açıklaması

Satış siparişleri ve transfer emirleri için maddeleri atlayamazsınız ve kısmi malzeme çekme yapamazsınız.

### <a name="issue-resolution"></a>Sorunun çözümü

**Mobil cihaz menü öğeleri** sayfasında, satış siparişlerini veya transfer emirlerini işleyecek şekilde ayarlanan her menü öğesi için **Genel** hızlı sekmesindeki **İşin bölünmesine izin ver** seçeneğini *Evet* olarak ayarlayın.

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a>Kısmi miktarlı iş için stok durumu değişikliğini nasıl yapabilirim?

### <a name="issue-description"></a>Sorun açıklaması

Partinin kısmi bir miktarı için stok durumu değişikliği yapmak istiyorsunuz.

### <a name="issue-resolution"></a>Sorunun çözümü

Çalışanların bu değişikliği yapmasını sağlamak için Ambar Yönetimi mobil uygulamasında bir menü öğesi oluşturabilirsiniz. **Mobil cihaz menü öğeleri** sayfasında, şu özelliklere sahip bir menü öğesi oluşturun (veya düzenleyin):

- **Mod:** *İş*
- **Varolan çalışmayı kullan:** *Hayır*
- **İş oluşturma işlemi:** *Hareket*
- **Stok durumunu görüntüle:** *Evet*

Sayfadaki diğer alanları gerektiği gibi ayarlayabilirsiniz.

## <a name="the-dock-management-profile-of-a-location-profile-is-not-preventing-inventory-types-from-being-mixed"></a>Bir konum profilinin giriş/çıkış noktası yönetim profili stok türlerinin karıştırılmasını engellemiyor.

### <a name="issue-description"></a>Sorun açıklaması

*Sevkiyat konsolidasyonu ilkelerini* kullanıyorsunuz. Bir *konum profili* için bir *giriş/çıkış noktası yönetim profili* ayarladınız ancak iş oluşturulduğunda, stok türleri son konumda karıştırılır.

### <a name="issue-resolution"></a>Sorunun çözümü

Giriş/çıkış noktası yönetim profillerinin önceden bölünmesi için çalışma gerekir. Başka bir deyişle, giriş/çıkış noktası yönetim profili, bir iş başlığının birden çok yerleştirme konumuna sahip olmayacağını bekler.

Giriş/çıkış noktası yönetim profilinin stok karıştırmayı etkin bir şekilde yönetmesi için bir iş başlığı sonu ayarlanmalıdır.

Bu örnekte, giriş/çıkış noktası yönetim profilimiz, **Karıştırılmaması gereken stok türleri** *Sevkiyat Kimliği* olarak ayarlanacak şekilde yapılandırılmıştır ve bunun için bir iş başlığı sonu ayarlayacağız:

1. **Ambar yönetimi \> Kurulum \> İş \> İş şablonları**'na gidin.
1. Düzenlenecek **İş emri türünü** seçin (örneğin, *Satın alma siparişleri*).
1. Düzenlenecek iş şablonunu seçin.
1. Eylem Bölmesi'nde, **Sorgu düzenle**'yi seçin.
1. **Sıralama** sekmesini açın ve aşağıdaki ayarlara sahip bir satır ekleyin:
    - **Tablo** - *Geçici iş hareketleri*
    - **Türetilmiş tablo** - *Geçici iş hareketleri*
    - **Alan** - *Sevkiyat Kimliği*
1. **Tamam**'ı seçin.
1. **İş şablonları** sayfasına yönlendirilirsiniz. Eylem Bölmesinde **İş başlığı sonları**'nı seçin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **Alan adı** *Sevkiyat Kimliği* ile ilişkili onay kutusunu seçin.
1. Eylem bölmesinde, **Kaydet**'i seçin.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
