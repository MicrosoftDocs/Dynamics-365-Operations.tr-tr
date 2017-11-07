---
title: "Doğrudan teslimatlar"
description: "Bu makale, doğrudan teslimler hakkında genel bilgiler sağlar. Müşterinize doğrudan satıcı tarafından gönderilen teslimatlar, doğrudan teslimatlardır."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchCreateFromSalesOrder, SalesTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 9704
ms.assetid: 64c51384-8a4e-45d0-83c1-12cea22902f9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a62c1c78ae66ffff7e36fe17757bb98d2e7fbc54
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="direct-deliveries"></a>Doğrudan teslimatlar

[!include[banner](../includes/banner.md)]


Bu makale, doğrudan teslimler hakkında genel bilgiler sağlar. Müşterinize doğrudan satıcı tarafından gönderilen teslimatlar, doğrudan teslimatlardır.

Doğrudan teslimler, teslimat süresini kısaltır ve envanter taşınmasıyla ilgili maliyetleri düşürür, çünkü müşteriye göndermeden önce ürünleri deponuzda tutmanıza gerek yoktur.  

**Satış siparişi** sayfasından doğrudan teslimler oluşturabilirsiniz. Öncelikle bir satış siparişi ve sipariş satırları oluşturun. Ardından, İşlem Panosunda **Satış siparişi** sekmesinden **Doğrudan teslimat** seçimini yapın. Son olarak, doğrudan teslimat olarak işlenmesi gereken satırları seçin. Böylece doğrudan teslimat için satış siparişi satırları ile buna karşılık gelen satın alma emri satırları arasında bir bağlantı oluşturulur.  

**Not:** Sipariş edilen miktarın bir kısmı halihazırda teslime dilmişse kalan miktarın bölünmesi gerekir. Doğrudan teslim edilmesi gereken miktar için yeni bir satır girin ve bu miktarı orijinal satırdaki miktardan çıkarın. Örneğin, orijinal miktar 15 birim ise ve beş birim halihazırda teslim edilmişse kalan miktar olan 10 birim için yeni bir satır oluşturmanız ve orijinal miktardan bu miktarı çıkarmanız gerekir.  

Satış sipariş satırları ve satın alma emri satırları arasında doğrudan teslimat bağlantısı oluşturduktan sonra, satış siparişini bir sevk irsaliyesi kullanarak güncelleyebilirsiniz. Bir sevk irsaliyesi güncellemesi veya satın alma emrinden bir fatura güncellemesi yürütün. **Satış siparişi** sayfasından satış siparişi için faturayı güncellemeniz gerekir. Bir fatura güncellemesi, satış siparişindeki miktarın alındı olarak kaydedilen miktarı geçmesine neden olamaz. Örneğin, bir satış siparişi satırı 10 parça içeriyor, ancak bir sevk irsaliyesi kullanılarak satış sipariş satırındaki sadece beş parça güncellenmiş olsun. Satış siparişinde fatura güncellemesi yaptığınızda **Miktar** listesi altından **Tümü** seçimini yaparsanız sadece fiziksel olarak alınmış olan veya bir sevk irsaliyesi kullanılarak güncellenen ürünlerin faturaları güncellenir. Tüm satış siparişi satırı güncellenmez.

## <a name="delivery-date"></a>Teslimat tarihi
Satış siparişi satırındaki **Talep edilen alış tarihi** alanını güncellediğinizde ilgili satın alma emri satırındaki **Teslimat tarihi** alanı da güncellenir. Benzer şekilde, satın alma emri satırındaki **Onaylandı** alanını güncellediğinizde, karşılık gelen satış siparişi satırındaki **Onaylanan alım tarihi** ve **Onaylanan gönderi tarihi** alanları da güncellenir.

## <a name="delivery-address"></a>Teslimat adresi
Tipik olarak, bir satın alma emrinin teslim adresi şirketin adresidir. Ancak, yeni bir teslimat oluşturduğunuzda müşterinin adresini teslimat adresine girersiniz. Teslimat türü **Doğrudan teslimat** olan bir satın alma emri satırındaki teslimat adresini değiştirirseniz, buna karşılık gelen satış siparişi satırındaki teslimat adresi de güncellenecektir. Benzer şekilde, satış siparişi satırındaki teslimat adresini değiştirirseniz, satın alma emri satırındaki teslimat adresi de güncellenir.

## <a name="deleting-order-lines"></a>Sipariş satırları siliniyor
Teslimat türü **Doğrudan teslimat** olan bir satış siparişi satırını silmeye çalıştığınızda satın alma emri satırlarının bu satıra bağlı olduğunu açıklanan bir mesaj kutusu görüntülenir. Satış sipariş satırı kısmen teslim edildiyse, satış siparişi satırını veya bununla ilişkili satın alma emri satırını silemezsiniz.

## <a name="warehouse"></a>Ambar
Bir doğrudan sevkiyat oluşturduğunuzda, hiçbir zaman fiziksel olarak satmadığınız öğeler ambarınıza ulaşır. Ancak, satış emri satırında hala bir ambar belirtmeniz gerekir. Benzer şekilde, teslim alma gereksinimleri de ürün için ürün modeli grubunda tanımlanabilir. Ancak, ürünler fiziksel olarak hiçbir zaman ambarınıza ulaşmadığı için, satış siparişi bir doğrudan teslimat olduğunda bu gereksinimler göz ardı edilir.




