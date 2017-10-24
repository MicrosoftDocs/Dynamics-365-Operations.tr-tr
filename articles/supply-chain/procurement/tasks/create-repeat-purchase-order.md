--- 
title: "Tekrar eden satınalma siparişi oluşturma"
description: "Bu prosedür önceki satınalma siparişi belgesinden yeni bir PO veya mevcut PO'ya satırları kopyalayarak tekrar eden bir satınalma siparişinin (PO) nasıl oluşturulacağını gösterir."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 257582d889ff55753f9bdbd234f0540503d20f27
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-repeat-purchase-order"></a>Tekrar eden satınalma siparişi oluşturma

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu prosedür önceki satınalma siparişi belgesinden yeni bir PO veya mevcut PO'ya satırları kopyalayarak tekrar eden bir satınalma siparişinin (PO) nasıl oluşturulacağını gösterir. Tekrar eden siparişleri oluşturmak için iki yöntem vardır. Eylem Bölmesi'nden belge düzeyindeki kullanılabilir eylemleri kullanabilir veya satır ayrıntısı eylemlerini kullanabilirsiniz. Satır ayrıntıları eylemi temel olarak mevcut siparişe satır eklerken, belge düzeyi eylemleri satır ekleyerek yeni bir satınalma siparişi oluşturmak için tasarlanmıştır. Bu kılavuzda gösterilen örnek, demo veriler şirketi USMF'de kullanılabilir. Bu görev genellikle bir satınalma temsilcisi tarafından gerçekleştirilir.


## <a name="create-a-new-repeat-purchase-order"></a>Yeni bir tekrar eden satınalma siparişi oluşturun
1. Tedarik ve kaynak atama > Sipariş emirleri > Tüm sipariş emirleri öğesine gidin.
    * İlk olarak bilgileri yeni siparişe kopyalama seçeneğini deneyeceğiz.  
2. Yeni'ye tıklayın.
3. Satıcı hesabı alanına, US-101 girin.
4. Tamam'a tıklayın.
5. Eylem Bölmesi'nde, Satın alma siparişi'ne tıklayın.
6. Tümünden'e tıklayın.
    * Bu sayfadan mevcut siparişleri kendi siparişinize kopyalayabilirsiniz. Satırların nasıl kopyalandığına ilişkin farklı seçenekler ve kopyalama yapabileceğiniz farklı belge türleri vardır. İlk olarak satırların nasıl kopyalanacağını inceleyeceğiz.   
7. Parametreler bölümünü genişletin.
    * Miktar faktörü alanı, kopyalama yaptığınız sırada açık olandan farklı bir miktar kullanmanız gerekiyorsa yararlıdır. Örneğin; kopyaladığınız satırlardaki miktarı iki kez sipariş etmek isterseniz bu alana '2' yazarsınız ve sonra sistem orijinal miktarın ikiye katlandığı yere satır ekler.  
    * İşareti tersine çevir alanı da eklenen sipariş satırları için miktarın işaretini değiştirerek sipariş edilen miktarı değiştirmeyi destekler. Bu, hareketi iptal eden sipariş satırları oluşturularak hareketi tersine çevirmeniz gerektiğinde yararlı olabilir. Bu seçenek, sayfa Alacak dekontu oluştur eyleminde açıldığında otomatik olarak seçilir.  
    * Masrafları kopyala seçeneği, masrafları sipariş satırlarını kopyaladığınız belgedeki yeni siparişinize kopyalamanızı sağlar.  
    * Fiyatları yeniden hesapla seçeneği bunları diğer bilgileri kopyaladığınız belgeden kopyalamak yerine geçerli fiyatları ve indirimleri kullanır.  
    * Tam olarak kopyala seçeneği, sipariş belgesi başlığı ve satırları üzerindeki tüm alanlarda değerlerin tam bir kopyasını oluşturur. Bu seçenek seçilmezse yeni siparişi el ile oluşturuyormuş gibi satıcı ve ürünlerle ilgili birçok alan için varsayılan değerler kullanılır. Örneğin, kopyaladığınız sipariş satıcının varsayılan Fatura hesabını geçersiz kılarsa aynı Fatura hesabı siparişinize kopyalanır. Tam olarak kopyala seçeneğini seçmediyseniz satıcının varsayılan Fatura hesabı siparişinizde kullanılır.  
    * Satınalma satırlarını sil seçeneği, yeni satırları uygulamadan önce kopyaladığınız satınalma siparişinde halihazırda var olan tüm satınalma siparişi satırlarını siler. Uyarı vermeden mevcut tüm satırları sildiğinden bu seçeneği dikkatli kullanın.  
    * Sipariş başlığını kopyala seçeneğini kullanırsanız yeni siparişinizde başlık bilgilerini el ile oluşturmanız gerekmez. Bu seçeneğin satıcıyla ilişkili alanlar için varsayılan değerlerin kullanılmasına neden olacağını unutmayın. Kopyalama yaptığınız belgede kopyalamak istediğiniz varsayılan olmayan değerler varsa Tam olarak kopyala seçeneği de kullanın.  
8. Parametreler bölümünü daraltın.
    * Kopyalama yapabileceğiniz farklı belge kaynakları vardır ve her biri bu sayfa üzerinde ayrı bir bölüme sahiptir. Örneğin, Satın alma siparişleri bölümü mevcut satınalma siparişlerinden kopyalama yapmanızı sağlar.  
9. 00015 kodlu satınalma siparişi için satıra tıklayın. 
10. Onay kutusuna tıklayarak satırı seçin.
11. Siparişinize kopyalanmaması için satıra ait onay kutusunu temizleyin.
    * Şimdi, satınalma siparişinize eklemek için 4 satır seçildi. Diğer satınalma siparişlerinden ek satınalma siparişi satırlarının seçilmesi ve bunların siparişinize kopyalanması mümkündür. Satınalma belgelerinin diğer türlerinden de satır eklemek mümkündür. Sonraki birkaç adımda farklı seçenekler gözden geçirilir.  
12. Satın alma siparişleri bölümünü daraltın.
13. Onay bölümünü genişletin.
    * Kopyalama kaynağı olarak kullanmak için satınalma siparişi onaylarını buradan seçebilirsiniz. Satınalma siparişi onayları ilişkili satınalma günlüğü kimliği veya satınalma siparişi kimliği ile tanımlanır.  
14. Onay bölümünü daraltın.
15. Ürün girişleri bölümünü genişletin.
    * Kopyalama kaynağı olarak kullanmak için ürün girişi günlüklerini buradan seçebilirsiniz. Ürün girişi günlükleri ürün giriş fişi veya satınalma siparişi kimliği ile tanımlanır.   
16. Ürün girişleri bölümünü daraltın.
17. Faturalar bölümünü genişletin.
    * Kopyalama kaynağı olarak kullanmak için satıcı faturalarını buradan seçebilirsiniz. Faturalar, fatura fişi veya satınalma siparişi kimliğiyle tanımlanır.   
18. Faturalar bölümünü daraltın.
19. Seçilen satırlar veya kopyalanacak başlık bölümünü genişletin.
    * Bu görünüm siparişinize kopyalamak için seçilmiş tüm belgeler ve satırların özetini gösterir.   
20. Seçilen satırlar veya kopyalanacak başlık bölümünü daraltın.
21. Tamam'a tıklayın.
    * Seçtiğiniz 4 satır yeni satınalma siparişinize kopyalandı.   

## <a name="copy-lines-to-an-existing-purchase-order"></a>Satırları mevcut satınalma siparişine kopyalayın
    * Siparişin tamamını kopyalamak yerine yeni bir PO oluşturmak, PO başlığındaki bilgileri tamamlamak ve sonra mevcut siparişlerden tek tek satırları kopyalamak daha yaygın bir uygulamadır.  
1. Satınalma siparişi satırına tıklayın.
2. Tümünden'e tıklayın.
    * Sayfa önceden görüntülenenin aynısını açar ancak sipariş satırlarını görünümünden açıldığında farklı seçenekler seçilir. Parametreleri gözden geçirelim.   
3. Parametreler bölümünü genişletin.
    * Satınalma satırlarını sil seçeneği seçilmez. Bu, mevcut satırları kaldırmadan siparişinize yeni satırlar kopyalayabileceğiniz anlamına gelir.   
    * Siparişe yalnızca ek satırlar eklediğimizden Sipariş başlığını kopyala seçeneği de seçilmez.   
4. Parametreler bölümünü daraltın.
    * Bu örnekte, mevcut satınalma siparişinden satırları kopyalayacağız.   
5. 00034 kodlu satınalma siparişi için satıra tıklayın. 
6. Onay kutusuna tıklayarak satırı seçin.
    * Bu PO üzerinde tek sipariş satırının da seçildiğine dikkat edin.  
7. Tamam'a tıklayın.
    * Ek sipariş satırı satınalma siparişinize eklendi.  


