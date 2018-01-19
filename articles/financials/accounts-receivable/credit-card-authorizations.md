---
title: "Kredi kartı ayarlama, onaylama ve tutma"
description: "Bu makale, Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'da kredi kartı onayına genel bakışı sağlar. Nasıl ödeme hizmeti ayarlanacağı, satış emrine kredi kartı ekleneceği ve yetkilendirme iptal edileceğine dair bilgiler içerir."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, Retail
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 40d636cac477871f094286d29edc32cd5616ad44
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="credit-card-setup-authorization-and-capture"></a>Kredi kartı ayarlama, onaylama ve tutma

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Bu makale, Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'da kredi kartı onayına genel bakışı sağlar. Nasıl ödeme hizmeti ayarlanacağı, satış emrine kredi kartı ekleneceği ve yetkilendirme iptal edileceğine dair bilgiler içerir.

<a name="setting-up-the-credit-card-payment-service"></a>Kredi kartı ödeme hizmeti ayarlama
------------------------------------------

Kredi kartlarını kullanmak için, Ödeme hizmetleri sayfasından bir ödeme hizmeti ayarlamanız ve etkinleştirmeniz gerekir. Ödeme hizmeti, tüzel kişiliğiniz ile müşterinin kredi kartı harcamalarını işleyen banka arasında bir köprü olarak çalışır. Ödeme bağlayıcı alanında listelenen bir kredi kartı sağlayıcısıyla çalışmanız ve bu sağlayıcıyla bir hesap kurmanız gerekmektedir. Ardından Ödeme hizmetleri sayfasında diğer seçenekleri belirlemeniz, Kredi kartı türleri sayfasında American Express, Discover, MasterCard ve Discover için kredi kartı türlerini ayarlamanız ve sağlayıcıyı varsayılan sağlayıcı olarak etkinleştirmeniz gerekir. Ayrıca, ayarları tamamlamak için aşağıdaki adımları izlemeniz gerekir:
-   Alacak hesapları parametreleri sayfasında, kredi kartı onaylarını kullanmak için parametreleri belirtin.
-   Ödeme koşulları sayfasında, kredi kartları için ödeme koşullarını ayarlayın. Ödeme türü alanında Kredi kartı'nı seçin.
-   Müşteri kredi kartları sayfasında, müşteriler için kredi kartı bilgilerini girin.

## <a name="adding-a-new-credit-card"></a>Yeni kredi kartı ekleme
Müşteri, Ayar, Kredi kartı öğelerini kullanarak Müşteriler sayfasında yeni kredi kartı kayıtları oluşturabilirsiniz. Ayrıca, Satış siparişi sayfasında siparişleri girerken Yönet, Müşteri, Kredi kartı, Kaydet öğelerini kullanarak da kredi kartı kayıtları oluşturabilirsiniz.
Bir satış siparişine kredi kartı ekleme
-------------------------------------

Satış siparişi sayfasındaki Fiyat ve iskontolar hızlı sekmesindeki kredi kartı arama alanından bir kredi kartı seçerek satış siparişine kredi kartı ekleyebilirsiniz. Onay işlemini başlatmak için, Eylem Bölmesindeki Yönet sekmesinde Kredi kartı ve Onay öğelerini seçin.
Kredi kartını onaylama
-------------------------

Bir kredi kartı onaylanırken, kart numarası ve kart sahibinin adı doğrulanır ve kullanılabilir kredi bakiyesi onaylanır. İsteğe bağlı olarak, kart doğrulama değeri ve kart sahibinin adresi de doğrulanabilir. Ardından, müşterinin kullanılabilir kredi bakiyesinden fatura tutarı düşülür. Ödeme hizmeti, kredi kartının onaylandığı ya da reddedildiği bilgisini gönderir. Satış siparişi faturalandırıldığında, kredi kartı fatura tutarı ile borçlandırılır (tutulan).

### <a name="card-verification-value"></a>Kart doğrulama değeri

Bazen kredi kartı güvenlik kodu olarak belirtilen kart doğrulama değerini isteyebilirsiniz. Bu, American Express için dört basamaklı bir değerdir. Discover, MasterCard ve Visa için bu değer üç basamaklıdır.

### <a name="address-verification"></a>Adres doğrulama

Adres doğrulama bilgileri her zaman ödeme sağlayıcısına gönderilir. Bir hareketi kabul edilmesi için ne kadar bilginin gerekli olduğuna karar verebilirsiniz. Sağlayıcınızın bu bilgileri kabul edip edemeyeceğini kontrol ettiğinizden emin olun. Adres doğrulama seçenekleri şunlardır:
-   **Hareketi her zaman kabul et** – Adres doğrulama sonucuna bakılmaksınız hareketi kabul et.
-   **Hesap sahibi** – Harekette belirtilen kart sahibi adını kredi kartı şirketinin bilgileriyle karşılaştır.
-   **Fatura adresi** – Harekette belirtilen kart sahibi adını ve fatura adresini kredi kartı şirketinin bilgileriyle karşılaştır.
-   **Fatura posta kodu** – Harekette belirtilen kart sahibi adını, fatura adresini ve posta kodunu kredi kartı şirketinin bilgileriyle karşılaştır.

## <a name="data-support"></a>Veri desteği
Desteklenen her kredi kartı türü için veri desteği düzeyini belirtebilirsiniz. Bu düzey, bir hareketle ilgili ne kadar bilginin ödeme hizmetine aktarılacağını denetler. Sağlayıcınızın bu bilgileri sunup sunamayacağını kontrol edin. Veri desteği düzeyi seçenekleri şunlardır:
-   **Düzey 1** – Hareket tarihini, hareket tutarını ve açıklamayı aktar.
-   **Düzey 2** – Düzey 1'deki bilgilere ek olarak sevkiyat ve tüccar adresleri ile vergi bilgilerini aktar.
-   **Düzey 3** – Düzey 2'deki tüm bilgilere ek olarak sipariş satırı bilgilerini de aktar.

## <a name="partial-payments"></a>Kısmi ödemeler
Bir siparişin parçası olarak gönderirseniz, kısmi siparişin tutarı yakalanır ve tüm siparişin tutarı için olan yetkilendirme, kapatılır. Daha sonra yeni bir yetkilendirme, gönderilmemiş olan siparişin bir kalan tutarı için gönderilir.

## <a name="voiding-an-authorization"></a>Onayı hükümsüz kılma 
Kredi kartı onayını hükümsüz kılmak için, ödeme türü Kredi kartı olmayan başka bir ödeme yöntemi belirleyebilirsiniz.






