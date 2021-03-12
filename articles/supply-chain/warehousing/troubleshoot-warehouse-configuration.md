---
title: Ambar yapılandırması ile ilgili sorunları giderme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ı yapılandırırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 09b5770190fea9591f422b61ce6deedb2b9fa790
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994015"
---
# <a name="troubleshoot-warehouse-configuration"></a>Ambar yapılandırması ile ilgili sorunları giderme

[!include [banner](../includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ı yapılandırırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a>Şu hata iletisini alıyorum: "Plaka veya konum geçerli değil."

### <a name="issue-description"></a>Sorun açıklaması

Bu hata iletisini, bir plaka kimliğini veya konumu taradığınızda alırsınız.

### <a name="issue-resolution"></a>Sorunun çözümü

Plaka kimliğinin başka bir şey tarafından ayrılmadığından emin olun. Bu sorun, bir kullanıcının ambar uygulamasında taradığı değer, hem geçerli bir konum hem de geçerli bir plaka olduğunda oluşurdu. Ancak, bu sorun 10.0.11 sürümünde giderilmiştir.

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

## <a name="i-cant-use-the-warehouse-app-to-do-partial-picking"></a>Kısmi malzeme çekme yapmak için ambar uygulamasını kullanamıyorum.

### <a name="issue-description"></a>Sorun açıklaması

Satış siparişleri ve transfer emirleri için maddeleri atlayamazsınız ve kısmi malzeme çekme yapamazsınız.

### <a name="issue-resolution"></a>Sorunun çözümü

**Mobil cihaz menü öğeleri** sayfasında, satış siparişlerini veya transfer emirlerini işleyecek şekilde ayarlanan her menü öğesi için **Genel** hızlı sekmesindeki **İşin bölünmesine izin ver** seçeneğini *Evet* olarak ayarlayın.

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a>Kısmi miktarlı iş için stok durumu değişikliğini nasıl yapabilirim?

### <a name="issue-description"></a>Sorun açıklaması

Partinin kısmi bir miktarı için stok durumu değişikliği yapmak istiyorsunuz.

### <a name="issue-resolution"></a>Sorunun çözümü

Çalışanların bu değişikliği yapmasını sağlamak için ambar uygulamasında bir menü öğesi oluşturabilirsiniz. **Mobil cihaz menü öğeleri** sayfasında, şu özelliklere sahip bir menü öğesi oluşturun (veya düzenleyin):

- **Mod:** *İş*
- **Varolan çalışmayı kullan:** *Hayır*
- **İş oluşturma işlemi:** *Hareket*
- **Stok durumunu görüntüle:** *Evet*

Sayfadaki diğer alanları gerektiği gibi ayarlayabilirsiniz.
