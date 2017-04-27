---
title: "Stok kapanışı"
description: "Çıkış hareketlerinin giriş hareketleriyle kapatılması sürecinin bir parçası olarak, genel defterin yapılan düzenlemeleri yansıtacak şekilde güncellenmesini seçebilirsiniz."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-03-08 15 - 56 - 00
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventClosing
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 61973
ms.assetid: c210c882-6849-4704-b78c-a777dd6cfdb6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 4e8de5c43f9e309787e4490586c1eac3858fb9fc
ms.lasthandoff: 03/29/2017


---

# <a name="inventory-close"></a>Stok kapanışı

Çıkış hareketlerinin giriş hareketleriyle kapatılması sürecinin bir parçası olarak, genel defterin yapılan düzenlemeleri yansıtacak şekilde güncellenmesini seçebilirsiniz.

Stok kapanışı işlemi, maddenin madde modeli grubunda seçilen stok değerleme yöntemine dayanarak çıkış hareketlerini giriş hareketlerine karşılık kapatır. Kapatma işleminin parçası olarak, genel muhasebenin güncellenmesi gerektiğini belirleyebilir, böylelikle yapılan düzeltmeyi yansıtmasını sağlayabilirsiniz. Ancak, stok kapanış veya yeniden hesaplama çalıştırılana kadar, çıkış hareketleri hesaplanan cari ortalama maliyet fiyatından deftere nakledilir. Stok kapatmanın ardından, tamamlanan stok kapanış işlemini geri almadığınız sürece ayarladığınız stok kapanış tarihinden önce olan dönemlerde deftere nakil yapamazsınız. Örneğin, 31 Ocak'ta sona eren bir dönem için stok kapanışı çalıştırırsanız, 31 Ocak'tan önceki bir tarihe sahip hareketleri deftere nakledemezsiniz. Stoktaki maddeler iki stok türünden birine atanır: madde veya hizmet. Stok kapanışı, iki tür için de aynı işlemleri gerçekleştirir. Ancak, hizmet maddeleri için stok kapanışı yine de çıkışları girişlere kapatır. Stok kapanış işleminin ne sıklıkta çalıştırılacağı şirkete göre değişir. Ancak, hareket hacmi, stok kapanışını ne sıklıkta çalıştırmaya karar vereceğinizi belirlemenize yardımcı olmalıdır. Genelde, çoğu şirket ay sonu kapanışı ve mutabakat yordamlarının bir parçası olarak stok kapanışı çalıştırır.

## <a name="inventory-recalculation-and-the-general-ledger"></a>Stok yeniden hesaplaması ve genel muhasebe
Bir ay veya başka stok dönemi boyunca stokta veya genel muhasebede düzeltmeler gerekiyorsa, stok kapanışı yerine stok yeniden hesaplamasını çalıştırabilirsiniz. Stok yeniden hesaplaması düzeltmeler yapar ancak stok hareketlerine kapatma yapmaz. Stok yeniden hesaplaması sırasında eldeki stok düzeltilir, stok hareketleri düzeltilir ve stok yeniden hesaplamaları ile stok kapanışları çalıştırılır. Bu görevler orijinal stok hareketi ile bağlantılı tüm genel muhasebeyi etkiler. **Örnek** Bir satış emrinden satınalma emri oluşturduğunuzda, orijinal satış emri için kullanılan genel muhasebe hesapları güncellenir. Maddeye atanan madde grubuna yönelik genel muhasebe hesapları satış emri deftere nakledildikten sonra değiştirilmiş ve bir stok yeniden hesaplaması bir düzeltme tutarı oluşturmuş olsa bile, düzeltme tutarı orijinal genel muhasebe hesaplarına nakledilir. Düzeltilmiş tutar, maddeye atanmış olan yeni genel muhasebe hesaplarına nakledilmez. Güncelleştirme tamamlandıktan sonra, bu görevlerden biri dolayısıyla nakledilmiş genel muhasebe fişini inceleyebilirsiniz.

1.  **Kapanış ve düzeltme** sayfası üzerindeki **Genel bakış** sekmesinde, incelenecek güncelleştirmeyi seçin.
2.  **Ayrıntılar** ve daha sonra **Fiş** seçeneğini tıklatın.

## <a name="effects-of-the-inventory-close-process-on-the-general-ledger"></a>Stok kapatma işleminin genel muhasebeye etkileri
**Kapanış ve düzeltme** sayfasında gerçekleştirebileceğiniz görevlerin birçoğu genel muhasebede güncellemelere neden olur. Örneğin, eldeki stok düzeltmeleri yaptığınızda, stok hareketi düzeltmeleri yaptığınızda, stok yeniden hesaplamasını çalıştırdığınızda ve stok kapanışını çalıştırdığınızda genel muhasebe güncellenir. Bu görevler sonucu güncellenen genel muhasebe hesapları orijinal stok hareketlerine bağlanır. Örneğin, bir satış emri bir satınalma emrine kapatıldığında, orijinal satış emri için kullanılan genel muhasebe hesapları düzeltilir. Bu davranış, maddeye atanan madde grubuna yönelik genel muhasebe hesapları satış emri deftere nakledildikten sonra değiştirilse bile gerçekleşir. Stok kapanışı kapatma tutarı oluşturduktan sonra, kapatma tutarı maddeye atanan yeni genel muhasebe hesaplarına değil yine orijinal genel muhasebe hesaplarına nakledilir. Genel muhasebe stok kapanışını geri aldığınızda da güncellenebilir. **Notlar:**

-   Standart maliyet değerleme yöntemini kullanırsanız stok kapanışı gerekmez.
-   Kapanış prosedürünü çalıştırmadan önce, güncelleme sırasında kapatılamayacak maddelerin listesini görüntüleyebilirsiniz.
-   Bilgi işlem kaynaklarını daha düzgün dağıtmak için, stok kapanışını yoğun olmayan saatlerde çalıştırmanızı öneririz.

## <a name="the-inventory-close-log"></a> Stok kapanış günlüğü
Stok kapatma işlemi tamamlandıktan sonra, mesaj merkezindeki bir mesaj, size bir hareket tam olarak kapatılamadığı için bir birim maliyet fiyatının hatalı olabileceğini bildirebilir. Bu mesaj gösterilmeden önce, sistem madde sayısını ve etkilenen hareketi raporlar. Mesaj size bu hareket için kullanılan maliyet tutarının, stok kapatma yüzünden güncellenmediğini bildirir. Bu mesaj çıkış türünde bir hareket kapatılamadığında belirir. Stok kapatma işlemi sırasında, sistem her bir mali boyutu kontrol ederek belirtilen kapanış tarihine dek girişlerden daha fazla çıkış olup olmadığına bakar. Bu tür bir dengesizlik, bir stok hareketi satınalma emrinden mali olarak deftere tamamen nakledilmediğinde, ya satıcı faturası alınmadığından ya da bir üretime daha üst bir düzeyden dahil edilmiş ürün reçetesi (BOM) bileşenleri mali olarak deftere nakledilmediğinde gerçekleşebilir. (Alt üretim maliyet hesaplanmaz.) Bu durumda, sonraki kapanış yeterli giriş bilgisi olmadığından tüm çıkışları doğru maliyet fiyatına düzeltmeyecektir. Her bir kapanış prosedürü için sistem uyarılar içeren bir kaydın kaydedilip görüntülenip görüntülenmeyeceğini gösterir. Mesajda çok sayıda uyarı alıyorsanız, şu önlemleri uygulamanızı öneririz:

-   Girişleri mali olarak güncelleştirin.
-   Kapanış tarihini ileri alın.
-   İşletme prosedürlerini yeniden değerleyin.

Uyarılar hakkında hiçbir şey yapamayacağınız durumlar da olabilir. Örneğin, işaretleme kullanılırken, işaretli satınalma emri kapanış tarihinden sonraki bir mali tarihe sahipse, kapanış tarihi değiştirilemez.

## <a name="reversing-a-completed-inventory-close"></a>Tamamlanan bir stok kapanışını geri alma
Tamamlanan bir stok kapanışını ters çevirerek, kapatmaları düzeltmelerden önceki durumlarına geri almanızın gerekeceği durumlarla karşılaşabilirsiniz. Tamamlanmış bir stok kapanışını ters çevirdiğinizde, stok kapanışının kapsadığı dönemde nakil izni vermek için stok yeniden açılır. İlgili değişiklikler genel muhasebede de yapılabilir. Düzeltmeler yapmayı tamamladıktan sonra, çalıştığınız dönem için stok kapatmayı yeniden çalıştırabilirsiniz. **Not:** Sadece kapatılan son stok dönemi yeniden açılabilir. Önceki bir stok kapatmayı geri almak için, en son kapatmadan başlayarak takip eden her stok kapatmanın tek tek geri alınması gerekir.


