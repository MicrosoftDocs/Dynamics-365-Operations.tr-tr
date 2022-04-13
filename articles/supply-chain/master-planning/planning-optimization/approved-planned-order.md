---
title: Planlı siparişleri görüntüleme, yönetme ve onaylama
description: Bu konu, planlama optimizasyonunda planlı siparişlerin nasıl görüntüleneceği, yönetileceği ve onaylanacağı hakkında bilgi sağlar.
author: t-benebo
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: b8c17ab3934ec7bfaed710c33515243290bb8e2a
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468791"
---
# <a name="view-manage-and-approve-planned-orders"></a>Planlı siparişleri görüntüleme, yönetme ve onaylama

[!include [banner](../../includes/banner.md)]

Bu konu, planlama optimizasyonunda planlı siparişlerin nasıl görüntüleneceği, yönetileceği ve onaylanacağı hakkında bilgi sağlar.

## <a name="view-and-manage-planned-orders"></a><a name="view-planned-orders"></a>Planlı siparişleri görüntüleme ve yönetme

Planlı siparişleri, planlı siparişler listesi sayfasında görüntüleyebilir ve yönetebilirsiniz. Çalışmak istediğiniz planlı siparişlerin türüne bağlı olarak aşağıdaki konumlardan birine gidin:

- Master planlama \> Çalışma alanları \> Master planlama
- Master planlama \> Master planlama \> Planlı siparişler
- Üretim denetimi \> Üretim emirleri \> Planlı üretim emirleri
- Tedarik ve kaynak atama \> Satınalma siparişleri \> Planlı satınalma siparişleri
- Stok Yönetimi \> Gelen siparişler \> Planlı transferler
- Stok Yönetimi \> Giden siparişler \> Planlı transferler

## <a name="view-and-edit-the-status-of-planned-orders"></a>Planlanan sipariş durumlarını görüntüleme ve düzenleme

İlerlemenizi izlemeye veya planlı siparişin nasıl işlendiğini değiştirmenizi sağlamak için planlı siparişlerin **Durum** alanlarını kullanabilirsiniz. Aşağıdaki **Durum** değerleri mevcuttur:

- **İşlem görmedi** – Master planlama, planlı siparişler ürettiğinde siparişlere bu durum verilir. Bu duruma sahip planlı siparişler sonraki planlama çalışmasında silinir.
- **Tamamlandı** – Bu durum, planlı siparişin tamamlandığını gösterir. Planlı bir siparişi kesinleştirmemeye karar vermeniz halinde, durumunu *Tamamlandı* olarak manuel bir şekilde değiştirebilirsiniz. Sistemin, *İşlenmemiş* ve *Tamamlandı* durumlarını aynı şekilde kabul ettiğini unutmayın.
- **Onaylandı** – Bu durum, planlı siparişin kesinleştirme için onaylandığını gösterir. Planlı bir siparişi kesinleştirmek isterseniz siparişin durumunu *Onaylandı* olarak değiştirebilirsiniz. Planlı bir siparişte yapılmış düzenlemeleri tutmak istiyorsanız veya planlı bir siparişi kesinleştirmeyi planlıyorsanız siparişin durumunu *Onaylandı* olarak değiştirin. *Onaylandı* durumdaki planlı siparişler sabit olarak kabul edilir ve master planlama bunların tedarik edilmesini bekler. Bu nedenle, daha sonra master planlama çalışması sırasında değiştirilmez veya silinmezler. Bu davranışı başarmak için, planlama mantığı, master planlama sırasında eski plan versiyonundaki *Onaylandı* durumuna sahip planlı siparişleri yeni plan sürümüne kopyalar. *Onaylandı* durumuna sahip planlı siparişlerinin yalnızca belirli master plan içinde tedarik edildiğini unutmayın.

Tek bir planlı siparişin durumunu değiştirmek için [herhangi bir planlı sipariş listesi sayfasını açın ](#view-planned-orders), siparişi açın ve ardından aşağıdaki adımlardan birini izleyin:

- **Genel** hızlı sekmesinde, **Durum** alanının değerini değiştirin.
- Eylem Bölmesi'nde, **Planlı sipariş** sekmesindeki **İşlem** grubunda **Durumu değiştir**'i seçin.
- Siparişi onaylamak için Eylem Bölmesinde **Onayla**'yı seçin.

Birkaç planlı siparişin durumunu aynı anda değiştirmek için, [herhangi bir planlı sipariş listesi sayfasını açın ](#view-planned-orders), değiştirmek istediğiniz siparişlerin onay kutularını işaretleyin ve sonra aşağıdaki adımlardan birini izleyin:

- Eylem Bölmesi'nde, **Planlı sipariş** sekmesindeki **İşlem** grubunda **Durumu değiştir**'i seçin.
- Siparişleri onaylamak için Eylem Bölmesinde **Onayla**'yı seçin.

## <a name="approve-planned-orders"></a>Planlı siparişleri onaylama

Planlı siparişlerden kesinleştirilmiş sipariş oluşturma işleminde planlı siparişlerin onayını isteğe bağlı bir adımdır.

Aşağıdaki resim, onay iş akışı uygulamak için her bir planlı siparişe atanan **Durum** değerini nasıl kullanabileceğinizi gösterir. Onay işlemi uygulamak için, önceki bölümde açıklandığı şekilde her bir planlı sipariş için **Durum** değerini manuel olarak düzeltin.

![Planlı sipariş akışı.](media/approved-planned-orders-1.png)

> [!TIP]
> Değiştirilmiş planlı siparişleri onaylamanız önerilir. Aksi takdirde, düzenlemeler bir sonraki planlama çalıştırması tarafından yok sayılacaktır ve bunların üzerine yazılacaktır.

## <a name="additional-resources"></a>Ek kaynaklar

- [Kesinleşmiş planlı siparişler](planned-order-firming.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
