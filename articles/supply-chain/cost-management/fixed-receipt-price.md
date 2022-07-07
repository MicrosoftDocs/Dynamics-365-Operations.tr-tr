---
title: Sabit giriş fiyatı
description: Bu makalede, Microsoft Dynamics 365 Supply Chain Management'ta sabit giriş fiyatlarını nasıl yapılandırabileceğiniz ve kullanabileceğiniz açıklanmaktadır.
author: rachel-profitt
ms.date: 04/25/2022
ms.topic: article
ms.search.form: InventPosting, InventItemGroup, InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-04-25
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: d58e8dcc580bf9327cd89427530f59340e27f4aa
ms.sourcegitcommit: 78576abe5c7cbab1bb69d26c999b038e8c24873a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/13/2022
ms.locfileid: "8954706"
---
# <a name="fixed-receipt-price"></a>Sabit giriş fiyatı

[!include [banner](../includes/banner.md)]

**Sabit giriş fiyatı**, *Standart maliyet* veya *Hareketli ağırlıklı ortalama* dışında bir stok modeli kullandığınızda madde model grubunda sunulan bir seçenektir. Microsoft Dynamics AX'in önceki sürümlerinde, bu seçenek **Standart maliyet** olarak adlandırılmıştır. Yeni standart maliyet stok modeli Dynamics AX 2012'de kullanıma sunulduğunda bu seçenek **Sabit giriş fiyatı** olarak yeniden adlandırılmıştır. Bu makalede, Dynamics 365 Supply Chain Management'ta sabit giriş fiyatlarını nasıl yapılandırabileceğiniz ve kullanabileceğiniz açıklanmaktadır.

## <a name="about-fixed-receipt-prices"></a>Sabit giriş fiyatları hakkında

Bir madde için **Madde model grubu** sayfasındaki **Sabit giriş fiyatı** onay kutusunu işaretlediğinizde, sistem stok girişi için standart maliyet olarak giriş fiyatını kullanır. Bir ürün için yapılandırılan satınalma fiyatı ve varsayılan madde maliyeti fiyatı farklıysa aradaki fark **Sabit giriş fiyatı karı** veya **Sabit giriş fiyatı zararı** hesabına nakledilir ve **Stok deftere nakil profili** sayfasında belirttiğiniz **Sabit giriş fiyatı mahsup işlemi** hesabına mahsup edilir.

**Sabit giriş fiyatı** seçeneği, farklı stok modelleriyle birlikte kullanıldığında (ör. ilk giren ilk çıkar (FIFO); son giren ilk çıkar (LIFO) ve ağırlıklı ortalama), *Stok kapatma ve ayarlama* işlemi **Madde modeli grubu** sayfasında seçtiğiniz stok ilkesine göre kapatma ve düzeltme oluşturmaya devam eder. Ancak, düzeltmeler yalnızca stoktan yapılacak çıkışlarda gerçekleştirilir.

Örneğin, **Stok modeli** alanının *FIFO* olarak ayarlandığı ve **Sabit giriş fiyatı** seçeneğinin seçildiği bir madde modeli grubuyla bir ürün yapılandırıyorsunuz. Satınalma siparişi üzerinden stok aldığınızda, stok değeri maddenin ürün girişi sırasındaki varsayılan maliyet fiyatı değerine ayarlanır. Satınalma siparişini faturaladığınızda, fatura fiyatı farklıysa, sistem serbest bırakılan ürünün varsayılan maliyet fiyatını stok hesabına nakleder. Farkı sabit giriş fiyatı karı veya zararı hesabına nakleder. Daha sonra, ürünü sattığınızda veya tükettiğinizde sistem, satış siparişi faturasının deftere nakledildiği sırada madde için ortalamayı kullanır (işaretleme kullanmadığınız takdirde).

*Stok kapatma ve ayarlama* işlemini çalıştırdığınızda sistem, ilk girişe karşı ilk çıkışla bir kapatma oluşturur. Girişte kullanılan giriş fiyatı ve çıkışta kullanılan ortalama arasındaki fark yeni bir fişe nakledilir.

## <a name="enable-fixed-receipt-prices"></a>Sabit giriş fiyatlarını etkinleştirme

Bir maddeyle ilgili sabit giriş fiyatlarını etkinleştirmek için, aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Kurulum \> Stok \> Madde modeli grupları** öğesine gidin.
2. Yeni bir madde model grubu oluşturun veya mevcut model grubunu seçin.
3. **Maliyetlendirme yöntemi ve maliyet tanıma** hızlı sekmesinde, **Sabit giriş fiyatı** onay kutusunu seçin.

    > [!NOTE]
    > **Stok modeli** alanı *Standart maliyet* veya *Hareketli ortalama* olarak ayarlanmışsa, **Sabit giriş fiyatı** onay kutusunu seçemezsiniz.

4. Sayfayı kapatın.

**Sabit giriş fiyatı** seçeneğini etkinleştirdiğinizde, aşağıdaki adımları izleyerek stok deftere nakil profilinizi güncelleştirmeniz gerekir.

1. **Stok Yönetimi \> Kurulum \> Deftere nakil \> Deftere nakil** sayfasına gidin.
1. **Satınalma siparişi** sekmesindeki **Seç** sütununda, **Sabit giriş fiyatı karı** seçeneğini belirleyin.
1. Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin.
1. Yeni satırı ayarlayın. Böylece yeni satır, sabit giriş fiyatını etkinleştirdiğiniz madde model grubu için geçerli olur. Satınalma siparişleri için sabit giriş fiyatı karlarını kaydetmek üzere kullanılan ana hesabı belirtin. Gereken şekilde diğer ayarları yapılandırın.
1. **Seç** sütununda, **Sabit giriş fiyat zararı** seçeneğini belirleyin. Sabit giriş fiyatını etkinleştirdiğiniz madde model grubu için geçerli olacak yeni bir satır ekleyin ve satınalma siparişleri için sabit giriş fiyatı zararlarını kaydetmek üzere kullanılan ana hesabı belirtin. Gereken şekilde diğer ayarları yapılandırın.
1. **Seç** sütununda, **Sabit giriş fiyatı mahsup işlemi** seçeneğini belirleyin. Sabit giriş fiyatını etkinleştirdiğiniz madde model grubu için geçerli olacak yeni bir satır ekleyin ve satınalma siparişleri için sabit giriş fiyatı mahsup işlemlerini kaydetmek üzere kullanılan ana hesabı belirtin. Gereken şekilde diğer ayarları yapılandırın.
1. **Stok** sekmesindeki **Seç** sütununda, **Sabit giriş fiyatı karı** seçeneğini belirleyin. Sabit giriş fiyatını etkinleştirdiğiniz madde model grubu için geçerli olacak yeni bir satır ekleyin ve stok için sabit giriş fiyatı karlarını kaydetmek üzere kullanılan ana hesabı belirtin. Gereken şekilde diğer ayarları yapılandırın.
1. **Seç** sütununda, **Sabit giriş fiyat zararı** seçeneğini belirleyin. Sabit giriş fiyatını etkinleştirdiğiniz madde model grubu için geçerli olacak yeni bir satır ekleyin ve stok için sabit giriş fiyatı zararlarını kaydetmek üzere kullanılan ana hesabı belirtin. Gereken şekilde diğer ayarları yapılandırın.

> [!NOTE]
> Genellikle **Sabit giriş fiyatı karı** ve **Sabit giriş fiyatı zararı** alanlarının hem satınalma siparişleri hem de stok için aynı ana hesabı kullanmasını öneririz.

> [!IMPORTANT]
> **Serbest bırakılan ürünler** sayfasının **Maliyetleri yönet** hızlı sekmesindeki **Fiyat** alanında bulunan değeri değiştirdiğinizde sistem, eldeki stoğu otomatik olarak yeniden değerlemez. El ile gerçekleştirilen geçici çözüm olarak, **Kapatma ve ayarlama** sayfasını açın ve Eylem Bölmesinde **Ayarlama \> Eldeki** seçeneğini belirleyin. Ardından stokta olan maddeleri seçin ve bunları geçerli fiyata göre ayarlayın. Standart maliyet stok modelinin kullanılmasının net avantajlarından biri, sistemin eldeki stoku otomatik olarak yeniden değerlemesine neden olmasıdır.
