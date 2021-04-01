---
title: Menşei ülke
description: Birçok kuruluş, ürünlerin belirli sertifika standartlarına uygun olmasını sağlamak için satıcılarına sertifika verir. Bu sertifikalar genellikle menşei ülkeye bağlıdır. Bu konu, bir ürünü kendi menşei ülkesine bağlamanıza ve ürün sertifikalarını izlemenize olanak sağlayan, menşei ülke özelliği hakkında bilgi sağlar.
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: COOVendorCerts
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: bb35770f32c21a685b21a41dc7c369ee01fe3891
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243309"
---
# <a name="country-of-origin"></a>Menşei ülke

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Birçok kuruluş, ürünlerin belirli sertifika standartlarına uygun olmasını sağlamak için satıcılarına sertifika verir. Bu sertifikalar genellikle menşei ülkeye bağlıdır. Menşei ülke özelliği, bir ürünü kendi menşei ülkesine bağlamanıza ve ürün sertifikalarını izlemenize olanak sağlar.

## <a name="turn-on-the-country-of-origin-feature"></a>Menşei ülke özelliğini açma

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ürün bilgileri yönetimi*
- **Özellik adı:** *menşei ülke yönetim özelliği*

## <a name="configure-source-and-destination-countries"></a>Kaynak ve hedef ülkeleri yapılandırma

Bir ürünle ilgili sertifika vermeden önce, ürünü hedef ülkesine ve menşei ülkesine bağlamanız gerekir.

1. **Ürün bilgileri yönetimi \> Kurulum \> Ürün uyumluluğu \> Menşei ülke \> Menşei ülke kuralları**'na gidin.
2. Düzenlemek için mevcut bir ülke kurulumu seçin veya Eylem Bölmesinde **Yeni**'yi seçerek yeni bir ülke kurulumu oluşturun.
3. Seçili veya yeni ülke için aşağıdaki değerleri ayarlayın.

    | Alan | Tanım |
    |---|---|
    | Madde kodu | Ürünün madde numarasını seçin. |
    | Hedef ülke | Ürünü göndereceğiniz ülkeyi seçin. |
    | Menşei ülke | Ürünü göndereceğiniz kaynak ülkeyi seçin. |

Bu kurulumun amacı, menşei ve hedef ülkelerin belirtildiği her bir parça için menşei ülkeyi ekleyebileceğiniz bir ürün reçetesi (BOM) raporu üretmeye yardımcı olmaktır. Bu rapor, parçaların nereden geldiğini ve nereye gideceğini bütünsel bir şekilde almanıza yardımcı olur.

## <a name="keep-track-of-vendor-certificates"></a>Satıcı sertifikalarını izleme

Satıcılara verdiğiniz sertifikaları izlemek için **Menşei ülke satıcı sertifikaları** sayfasını kullanabilirsiniz.

Hangi sertifika belgelerini düzenleyeceğinizi ve bunları müşterilere nasıl bildireceğinize karar vermeniz gerekir. Bu özellik, sertifikalarınızı izlemenize yardımcı olur. Ayrıca, ilgili sertifika numaralarının faturalarda, sevk irsaliyelerinde ve/veya sipariş onaylarında görünüp görünmeyeceğini seçmenize de olanak tanır.

Sertifika bilgilerinizi ayarlamak için aşağıdaki adımları izleyin.

1. **Ürün bilgileri yönetimi \> Kurulum \> Ürün uyumluluğu \> Menşei ülke \> Menşei ülke satıcı sertifikaları**'na gidin.
2. Düzenlemek için mevcut bir sertifika kurulumu seçin veya Eylem Bölmesinde **Yeni**'yi seçerek yeni bir sertifika kurulumu oluşturun.
3. Seçili veya yeni sertifika için aşağıdaki ayarları yapın.

    | Alan | Tanım |
    |---|---|
    | Satıcı hesabı | Sertifikanın verileceği satıcıyı seçin. |
    | Madde kodu | Sertifikanın verileceği ilgili maddeyi seçin. |
    | Ülke/bölge | Bu sertifikayı kullanmanız gereken hedef ülke veya bölge. |
    | Sertifika numarası | Düzenlediğiniz sertifikanın kimlik numarasını girin. |
    | Etkin | Geçerli sertifikanın geçerli olduğu ilk tarihi seçin.|
    | Bitiş tarihi | Geçerli sertifikanın geçerli olduğu son tarihi seçin. |
    | Faturaya yazdır | Belirtilen tarih aralığında belirtilen ülkeye yönelik faturalara sertifika numarası yazdırmak için bu onay kutusunu seçin. |
    | Sevk irsaliyesine yazdır | Belirtilen tarih aralığında belirtilen ülkeye yönelik sevk irsaliyelerine sertifika numarası yazdırmak için bu onay kutusunu seçin. |
    | Satış siparişine yazdır | Belirtilen tarih aralığında belirtilen ülkeye yönelik satış siparişlerine sertifika numarası yazdırmak için bu onay kutusunu seçin. |

## <a name="include-the-country-of-origin-on-bom-reports"></a>BOM raporlarında menşei ülke ekleme

Bir ürün reçetesi raporu oluştururken, kaynak ve hedef ülkeleri belirttiğiniz her bir parça için **Menşei ülke kuralları** sayfasına bulunduğu ülkeyi dahil edebilirsiniz.

1. **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. **Serbest bırakılan ürün ayrıntıları** sayfasını açmak için bir ürün oluşturun veya açın.
1. Eylem Bölmesinde, **Mühendis** sekmesindeki **BOM** gurubunda **Tasarımcı**'yı seçin.
1. Eylem Bölmesi'nde görüntülenen liste sayfasında **BOM \> Yazdır**'a tıklayın.
1. **Ürün reçetesi satırları** iletişim kutusunda, **Hedef ülke** alanını raporunuzda görüntülemek istediğiniz hedef ülkeye ayarlayın.
1. **Tamam**'ı seçin.

Her bir parçanın menşei ülkesi hakkında bilgi gösteren bir rapor oluşturulur ve gösterilir. Burada rapor için bir örnek verilmiştir.

![Menşei ülke raporu](media/country-of-origin-report.png "Menşei ülke raporu")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]