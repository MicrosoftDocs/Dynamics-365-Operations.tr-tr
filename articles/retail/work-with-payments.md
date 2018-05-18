---
title: "Bir çağrı merkezindeki ödeme yöntemleri"
description: "Bu konu Microsoft Dynamics 365 for Retail'de bir çağrı merkezinde kullanabileceğiniz farklı ödeme yöntemlerini ele alır."
author: josaw1
manager: AnnBe
ms.date: 03/28/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: MCRSalesTableOrderHistory, MCRCCAuthManagement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 92163
ms.assetid: 8e738907-870b-466c-ab0c-07f4a4aa47f3
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fe8dd3136f14e182e261a4dce57eef0b1946d304
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---

# <a name="payment-methods-in-a-call-center"></a>Bir çağrı merkezindeki ödeme yöntemleri

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 for Retail'deçağrı merkezi kanalı yapılandırması **Sipariş tamamlamayı etkinleştir** adında bir ayar içerir. Bu ayar kanal kullanıcılarının oluşturduğu tüm siparişlerin, yalnızca ön ödeme veya onaylanan tolerans dahilinde ödeme ön onayı olması durumunda sipariş işleme için serbest bırakılmasını sağlamaya yardımcı olur. **Sipariş tamamlamayı etkinleştir** ayarı açık olursa, çağrı merkezi kullanıcıları Çağrı merkezi ödeme işleme özelliklerini kullanarak müşteriler için satış siparişlerine karşı ödemeleri girebilirler. Bu ayar devre dışı bırakılırsa, çağrı merkezi kullanıcıları çağrı merkezi ödeme işleme özelliklerini kullanamaz ancak standart Alacak hesapları işlevini kullanarak satış siparişlerine ön ödemeleri uygulayabilirler.

Kanal yapılandırmasının bir parçası olarak şirket bir çağrı merkezi kanalı için izin verilen ödeme yöntemleri tanımlayabilir. Çağrı merkezi kanalı perakende mağaza kanalları için tanımlananlarla aynı ödeme yöntemlerini kullanır.

Bir çağrı merkezi kanalı için ödeme yöntemlerini yapılandırmak üzere **Perakende** \> **Kanallar** \> **Çağrı merkezleri** \> **Tüm çağrı merkezleri**'ne gidin ve **Kurulum** menüsünde **Ödeme yöntemleri** seçeneğini seçin.

Bir ödeme yöntemi oluşturduğunuzda, atayabileceğiniz beş ödeme yöntemi işlevi bulunur.

| İşlev            | Tanım |
|---------------------|-------------|
| Normal              | Nakit veya fiş gibi ödeme yöntemleri tanımlarken ödeme yönteminizde **Normal** işlevini kullanın. Bu tür ödemeler çağrı merkezindeki bir satış siparişine uygulandığında, müşteri hesabında hemen ön ödemeler olarak deftere nakledilir. Ön ödeme fişi müşterinin hareket geçmişinde deftere nakledilir ve burada faturalar oluşturulduğunda satış siparişi faturasına karşı sistematik olarak kapatılacaktır. |
| Denetle               | Ödeme yöntemi olarak bir banka çeki tanımladığınızda **Çek** işlevini kullanın. Bir satış siparişine bu ödeme türü uygulandığında, kullanıcının ödeme uygulama işleminin bir parçası olarak müşterinin çek numarasını girmesi gerekir. Çek ödemeleri uygulandıklarında daima ön ödeme olarak kabul edilir. **Normal** ödeme işlevinde, bu ön ödeme fişleri sistematik olarak sipariş için oluşturulan faturalara karşı kapatılır. |
| Kartlar               | Kart ödeme türleri müşterinin ödeme kartı üzerinde tanımlanmış olan bir kart numarasının girilmesini gerektiren herhangi bir ödeme türünü temsil eder. Hediye kartları ve kredi kartları örnek olarak verilebilir. Bu tür ödemeleri yapılandırırken bu ödeme yöntemiyle ilişkilendirilen kart kodlarını tanımlamak için **Kart kurulumu** menüsünü kullanmanız gerekir. Siparişi girerken kullanıcılar kart ödemesinin ön ödeme mi olacağını ödeme girişi sayfasında görüntülenen **Ön ödeme** seçeneğini kullanarak belirtebilir. İşletme ön ödemeleri gerekli kılmadığı sürece, gerçek kredi kartı ödemesinin tipik akışı iki adımlı bir süreçtir; sipariş girişi sırasında yetki alınır ve ardından ödeme kapatılır ve faturalama sırasında müşterinin kartından tahsil edilir. Hediye kartı ödemeleri için, hediye kartı bakiyesinin hemen düşülerek müşterinin aynı değeri başka yerde uygulamasını önlemek gerekli olduğundan, ön ödeme önerilir. |
| Müşteri            | Bir ödeme yöntemindeki **Müşteri** işlevi ödemenin müşterinin kredi limitine uygulanacağı veya "açık hesaba" konulacağı anlamına gelir Retail'de, bir müşteriye sipariş girişi sırasında doğrulanabilen bir kredi limiti atanabilir. **Müşteri** işlevine bağlı bir ödeme yöntemi kullanılarak yapılan ödemeler müşteri hesabına karşı bir borç oluşturur. Satış siparişi faturalandığında, borç bakiyesi gösterilir. Bu durumlarda, müşteriler verilen koşullara göre tipik olarak bir ödeme gönderir. Alternatif olarak, müşteri hesabında daha önceden açılmış olan bir kredi fişi vadesi gelen bakiyeyi kapatmak için uygulanabilir. Bu ödeme yöntemini tanımlamış olsanız bile, **Hesap üzerinde izin ver** bayrağı üzerinde çalıştığınız müşteri için müşteri kaydında ayarlanmadıkça, çağrı merkezi sipariş girişi ödeme seçenekleri arasında görünmez. Bu bayrak müşteri kaydının **Ödeme varsayılanları** sekmesinde bulunur. |
| Ödeme Kaldırma/Kaydırma | **Ödeme Kaldırma/Kaydırma** işlevi çağrı merkezi tarafından kullanılmaz. Bu yalnızca satış noktası (POS) uygulamasının mağaza kanalında kullandığı ödeme yöntemlerini tanımladığınızda kullanılır. |

Ödeme yöntemleri tanımlandığında, bir genel muhasebe veya banka hesabına bağlanmalıdır. Bu adımı atlarsanız, kullanıcılar ödeme türünü kaydetmeye çalışırken hatalar alır.

## <a name="refund-payment-methods"></a>Geri ödeme yöntemleri

Geri ödeme işleme senaryoları için Çağrı merkezi Alacak hesaplarında tanımlanan ödeme yöntemlerinden bazılarını da kullanır. Bu ödeme yöntemlerini yapılandırmak için **Perakende** \> **Kanal kurulumu** \> **Çağrı merkezi kurulumu** \> **Çağrı merkezi geri ödeme yöntemleri**'ne gidin. Müşterilere geri ödeme çeklerini işlemek için bu yapılandırmayı tamamlamanız gerekir. Örneğin, bir müşteri bir siparişin ödemesini başlangıçta nakit veya çek kullanarak yaptıysa, kullanıcı müşteriye Alacak hesapları üzerinden bir geri ödeme çeki göndermek isteyebilir. Bu durumda, geri ödemenin düzgün şekilde gerçekleştirilebilmesi için çağrı merkezindeki çek ve nakit ödeme türlerinin Alacak hesaplarındaki doğru ödeme yöntemiyle eşlenmesi gerekir.

Ayrıca, bir kullanıcı Retail'de bir iade siparişini çağrı merkezi kullanıcısı olarak işlerse ancak iadeyi orijinal satışa bağlayamazsa **İade** ödemesi yönteminin Çağrı merkezi parametrelerinde tanımlanması gerekir. **Perakende** \> **Kanal kurulumu** \> **Çağrı merkezi kurulumu** \> **Çağrı merkezi parametreleri**'ne gidin ve **RMA/İade** sekmesindeki **Ödeme yöntemi** alanında bir ödeme yönteminin tanımlandığından emin olun. Ödeme yöntemi geri ödemeler için kullanılan ödeme yöntemi olacaktır. Genellikle, bir çek yöntemi veya müşteri hesabı yöntemi olarak tanımlanacaktır.

