---
title: Satış siparişlerinde gelir kabulü
description: Bu konuda, satış siparişleri ve faturalardaki geliri kabul etme konusunda temel işlevler açıklanmaktadır. Gelir kabulü, satış siparişinde ve satış siparişinden oluşturulan ilgili faturada kullanılabilir.
author: kweekley
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: f7d2cfb8e58221004ae5662aae3850adc577dc88
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570322"
---
# <a name="revenue-recognition-on-sales-orders"></a>Satış siparişlerinde gelir kabulü

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Gelir kabulü özelliği Özellik yönetiminden açılamaz. Şu anda, bu özelliği etkinleştirmek için yapılandırma anahtarları kullanmanız gerekir.

Bu konuda, satış siparişleri ve faturalardaki geliri kabul etme konusunda temel işlevler açıklanmaktadır. Gelir kabulü, satış siparişinde ve satış siparişinden oluşturulan ilgili faturada kullanılabilir. Satış siparişi ayrıca bir Zaman ve malzeme projesi üzerinden de oluşturulabilir.

> [!NOTE]
> Bu konudaki çizimlerde, kavramları daha iyi göstermek için sütunlar gizlenmiş veya kılavuzlara eklenmiştir. Bu nedenle çizimlerdeki sayfalar ve veriler, üründe gördüklerinizden farklı olabilir.

## <a name="enter-a-sales-order"></a>Satış siparişi girme

Aşağıdaki satış siparişi girilir ve gelir kabulü için ayarlanan üç madde eklenir.

[![Satış siparişi girme](./media/revenue-recognition-so-basic-sales-order-header.png)](./media/revenue-recognition-so-basic-sales-order-header.png)

Gelir kabulü için iki kavram vardır:

- **Gelir fiyatını belirleyin.** Gelir fiyatı, serbest bırakılan ürünlerin kurulumuna göre hesaplanır. Gelir fiyatı, müşteriye hiçbir zaman gösterilmez ancak yalnızca satış siparişi faturasının muhasebesi için kullanılır. Satış siparişi satırları ve satışın parçası olarak yazdırılan belgelerde birim/liste fiyatı gösterilmeye devam eder.
- **Gelir kabulünün uygulanması gereken zamanı belirleyin.** Gelir planı, gelirin kabul edilmesi gereken zamanı belirlemek için kullanılır.

    Bu örnekte ilk madde olan S0001, **1O** (bir tekrar) gelir planına atanır. Bu satır, gelecekte yükleme gerçekleştikten sonra gelirin kabul edileceği bir kilometre taşı türü senaryoyu temsil eder. Bu nedenle gelir, yükleme tamamlanana kadar ertelenir.

    İkinci madde olan S0008, sözleşme desteğini deftere naklet (PCS) maddesi olarak ayarlanan bir servis maddesidir. Sürdürülen mühendislik servisleri, müşteriye 12 aylık dönem üzerinden sağlanır. Bu nedenle, **12M** gelir planı varsayılan olarak ürüne atanır. Bu madde bir PCS maddesi olduğundan sözleşme başlangıç ve bitiş tarihlerinin tanımlanması gerekir. Varsayılan olarak sözleşme başlangıç ve bitiş tarihleri, Madde ayrıntıları – Kurulum sekmesinde bulunur. Gelir planında **12M** için kurulum, aşağıdaki çizimde gösterildiği gibi sözleşme şartları otomatik olarak doldurulacak şekilde tanımlanır.

    [![Gelir planları](./media/revenue-recognition-so-basic-revenue-schedules.png)](./media/revenue-recognition-so-basic-revenue-schedules.png)

    Üçüncü madde olan S0012 donanımdır ve hiçbir gelir planı varsayılan olarak atanmaz. Donanım için gelir, madde faturalandığında kabul edilir.

## <a name="confirm-the-sales-order"></a>Satış siparişini onaylama

Gelir fiyatı ve gelir planı hakkında ek ayrıntıları görüntülemek için satış siparişinin Eylem Bölmesi'ndeki **Yönet** sekmesinde **Gelir kabul** grubunda bulunan düğmeleri kullanın. Bu noktada satış siparişi onaylanmadığından gelir kabulü için kullanılan düğmeler kullanılamaz. Bu düğmeler, satış siparişi karşılamaya yol açan aşamalar üzerinden ilerledikçe kullanılabilir veya kullanılamaz.

[![Satış siparişi başlığı](./media/revenue-recognition-so-basic-sales-order-header-02.png)](./media/revenue-recognition-so-basic-sales-order-header-02.png)

İlk üç düğme, gelir kabulü için satış siparişi kurulumundaki maddelere yönelik gelir fiyatı hakkında ayrıntılar sağlar.

- **Gelir fiyatı tahsisatı**: Bu düğme, satış siparişi onaylandıktan veya fatura deftere nakledildikten sonra kullanılabilir. Hem satış siparişi onayı hem de faturanın deftere nakil işlemi, fiyatı muhasebe girişinde kabul edecek veya erteleyecek şekilde geliri hesaplar. Kuruluma göre hesaplanan gelir fiyatı, müşteriye gösterilen birim fiyattan farklı olabilir.
- **Yeni sipariş satırlarıyla fiyatı yeniden tahsis et**: Bu düğme, satış siparişi onaylandıktan veya fatura deftere nakledildikten sonra kullanılabilir. Yeniden tahsisat işlemi, faturalandıktan sonra geçerli satış siparişine veya yeni bir satış siparişine yeni satırın eklenmesinden sonra kabul edilmesi gereken geliri yeniden hesaplamak için kullanılır. Her iki durumda da yeni maddenin eklenmesi sözleşmede değişikliğe neden olur. Bu nedenle, gelir fiyatının yeniden tahsis edilmesi gerekir.
- **Gelir fiyatı tahsisatını güncelleştir**: Bu düğme, satış siparişi onaylandıktan sonra kullanılabilir ancak satış siparişi faturalandıktan sonra kullanılamaz. Güncelleştirme, satış siparişinin onaylanmasına gerek olmaksızın gelir fiyatı tahsisatını yeniden çalıştırmak için kullanılır. Satış siparişi faturalandıktan sonra gelir fiyatı yeniden hesaplanamaz.

Son iki düğme, bir gelir planı bulunan satış siparişindeki bu maddeler için gelir planıyla ilgili ayrıntılar sağlar.

- **Beklenen gelir kabulü planı**: Bu düğme, satış siparişi onaylandıktan sonra kullanılabilir ancak satış siparişi faturalandıktan sonra kullanılamaz. Beklenen gelir planını gösteren bir sayfa açar. Son plan gerçek sevk tarihini kullanırken beklenen plan talep edilen sevk tarihini kullandığından son plan değişebilir.
- **Gelir kabulü planı**: Bu düğme, satış siparişi faturalandıktan sonra kullanılabilir. Onay gerçekleştiğinde veya sevk irsaliyesi oluşturulduğunda son gelir kabulü planı oluşturulmaz. Yalnızca satış siparişi faturalandığında oluşturulur.

Aşağıdaki örnekte, satış siparişi onaylandığında gelir fiyatı tahsisatı gerçekleşmiştir. Gelir fiyatları farklı şekilde tahsis edilse bile **Kabul edilecek gelir** alanındaki toplam tutarın yine de müşteriye faturalanan satış siparişi satırlarının toplamına eşit olması gerektiğini unutmayın. Örneğin, satış siparişi satırlarının toplamı vergi hariç 1.499 Amerikan dolarıdır. Bu nedenle, **Kabul edilecek gelir** değerlerinin toplamı da 1.499 Amerikan doları olmalıdır.

[![Gelir fiyatı tahsisatı](./media/revenue-recognition-so-basic-revenue-price-allocation.png)](./media/revenue-recognition-so-basic-revenue-price-allocation.png)

Beklenen gelir kabulü planı da oluşturulur. Gelir planında, ertelenecek tutar olarak **Kabul edilecek gelir** değeri kullanılır. Madde S0001'de 300 Amerikan doları yerine 321,21 dolar ve madde S0008'de 100 dolar yerine 160,61 dolar ertelenir. Gelir ertelenmediğinden madde S0012 beklenen planda gösterilmez. Deftere nakil gerçekleşirken madde S0012, gelir genel muhasebe hesabına doğrudan 1.017,18 Amerikan doları nakleder.

[![Beklenen gelir kabulü planı](./media/revenue-recognition-so-basic-expected-rev-rec-schedule.png)](./media/revenue-recognition-so-basic-expected-rev-rec-schedule.png)

## <a name="create-the-packing-slip"></a>Sevk irsaliyesi oluşturma

Ardından, satış siparişi için sevk irsaliyesi oluşturulabilir. Sevk irsaliyesi deftere nakledildiğinde hiçbir gelir kabul edilmez. Satış siparişi onaylanmadıysa sevk irsaliyesinin deftere nakledilmesi gelir fiyatı hesaplamasını tetiklemez. Ayrıca beklenen veya son gelir kabulü planının oluşturulmasını da tetiklemez. Sevk irsaliyesinde geliri ertelemek için madde modeli grubu ayarlanırsa faturanın deftere nakledilmesinde kullanılan yeni ertelenen gelir hesaplarını değil, geçerli deftere nakil profili genel muhasebe hesaplarını kullanarak deftere nakletmeye devam eder.

## <a name="create-the-invoice"></a>Faturayı oluşturma

Son adım, satış siparişini faturalamaktır. Faturanın fişine bakarsanız madde S0001 ve S0008 için gelirin ertelendiğini (321,21 + 160,61 = 481,82 Amerikan doları) ve madde S0012 için kalan tutarın gelir olarak deftere nakledildiğini (1.017,18) görürsünüz. Bu değerler, satış siparişi satırlarının toplamıyla eşleşen 1.499 Amerikan doları kadardır.

[![Fiş hareketleri](./media/revenue-recognition-so-voucher-transactions.png)](./media/revenue-recognition-so-voucher-transactions.png)

Faturanın oluşturulmasının ardından gelir kabulü için **Gelir fiyatı tahsisatı**, **Yeni sipariş satırlarıyla fiyatı yeniden tahsis et** ve **Gelir kabulü planı** düğmeleri kullanılabilir ancak **Gelir fiyatı tahsisatını güncelleştir** ve **Beklenen gelir kabulü planı** düğmeleri kullanılamaz.

[![Kullanılabilir gelir kabulü düğmesinin kullanılabilirliği](./media/revenue-recognition-so-basic-after-invoice-buttons.png)](./media/revenue-recognition-so-basic-after-invoice-buttons.png)

**Gelir fiyatı tahsisatı** düğmesi gelir fiyatı hesaplamasını görüntüleyebileceğiniz şekilde yine de kullanılabilir. Onaylamanın ardından satış siparişinde hiçbir şey değişmediyse faturanın deftere nakledilmesi, **Kabul edilecek gelir** alanındaki hesaplanan tutarı değiştirmez.

Beklenen gelir kabulü planı kaldırılır ve son gelir kabulü planıyla değiştirilir. Gelir planı ayrıntıları her satış siparişi satırı için korunur ve sözleşme yükümlülükleri karşılandıkça ertelenen geliri gerçek gelire serbest bırakmak için kullanılır.

[![Son gelir kabulü planı](./media/revenue-recognition-so-revenue-recognition-schedule.png)](./media/revenue-recognition-so-revenue-recognition-schedule.png)
