---
title: Tekrar eden satınalma siparişi oluşturma
description: Bu konu önceki satınalma siparişi belgesinden yeni bir PO veya mevcut PO'ya satırları kopyalayarak tekrar eden bir satınalma siparişinin (PO) nasıl oluşturulacağını gösterir.
author: mkirknel
manager: tfehr
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchCopying
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b478e4cd5cf1eb88517bb923c377c6121d92fd0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204781"
---
# <a name="create-a-repeat-purchase-order"></a>Tekrar eden satınalma siparişi oluşturma

[!include [banner](../../includes/banner.md)]

Bu konu önceki satınalma siparişi belgesinden yeni bir PO veya mevcut PO'ya satırları kopyalayarak tekrar eden bir satınalma siparişinin (PO) nasıl oluşturulacağını gösterir. Tekrar eden siparişleri oluşturmak için iki yöntem vardır. Eylem Bölmesi'nden belge düzeyindeki kullanılabilir eylemleri kullanabilir veya satır ayrıntısı eylemlerini kullanabilirsiniz. Satır ayrıntıları eylemi temel olarak mevcut siparişe satır eklerken, belge düzeyi eylemleri satır ekleyerek yeni bir satınalma siparişi oluşturmak için tasarlanmıştır. Bu kılavuzda gösterilen örnek, demo veriler şirketi USMF'de kullanılabilir. Bu görev genellikle bir satınalma temsilcisi tarafından gerçekleştirilir.


## <a name="create-a-new-repeat-purchase-order"></a>Yeni bir tekrar eden satınalma siparişi oluşturun
1. Gezinti bölmesinde **Modüller > Tedarik ve kaynak atama > Satınalma siparişleri > Tüm satın alma siparişleri** öpesine gidin. İlk olarak bilgileri yeni siparişe kopyalama seçeneğini deneyeceğiz.  
2. **Yeni**'yi seçin.
3. **Satıcı hesabı** alanına `US-101` girin.
4. **Tamam**'ı seçin.
5. Eylem Bölmesi'nde, **Satın alma siparişi**'ni seçin.
6. **Tümünden**'i seçin. Bu sayfadan mevcut siparişleri kendi siparişinize kopyalayabilirsiniz. Satırların nasıl kopyalandığına ilişkin farklı seçenekler ve kopyalama yapabileceğiniz farklı belge türleri vardır. İlk olarak satırların nasıl kopyalanacağını inceleyeceğiz. 
7. **Parametreler** bölümünü genişletin.

    - **Miktar faktörü** alanı, kopyalama yaptığınız sırada açık olandan farklı bir miktar kullanmanız gerekiyorsa yararlıdır. Örneğin; kopyaladığınız satırlardaki miktarı iki kez sipariş etmek isterseniz bu alana '2' yazarsınız ve sonra sistem orijinal miktarın ikiye katlandığı yere satır ekler.  
    - **İşareti tersine çevir** alanı da eklenen sipariş satırları için miktarın işaretini değiştirerek sipariş edilen miktarı değiştirmeyi destekler. Bu, hareketi iptal eden sipariş satırları oluşturularak hareketi tersine çevirmeniz gerektiğinde yararlı olabilir. Bu seçenek, sayfa **Alacak dekontu oluştur** eyleminde açıldığında otomatik olarak seçilir.  
    - **Masrafları kopyala** seçeneği, masrafları sipariş satırlarını kopyaladığınız belgedeki yeni siparişinize kopyalamanızı sağlar.  
    - **Fiyatları yeniden hesapla** seçeneği bunları diğer bilgileri kopyaladığınız belgeden kopyalamak yerine geçerli fiyatları ve indirimleri kullanır.  
    - **Tam olarak kopyala** seçeneği, sipariş belgesi başlığı ve satırları üzerindeki tüm alanlarda değerlerin tam bir kopyasını oluşturur. Bu seçenek seçilmezse yeni siparişi el ile oluşturuyormuş gibi satıcı ve ürünlerle ilgili birçok alan için varsayılan değerler kullanılır. Örneğin, kopyaladığınız sipariş satıcının varsayılan Fatura hesabını geçersiz kılarsa aynı Fatura hesabı siparişinize kopyalanır. **Tam olarak kopyala** seçeneğini seçmediyseniz satıcının varsayılan Fatura hesabı siparişinizde kullanılır.  
    - **Satınalma satırlarını sil** seçeneği, yeni satırları uygulamadan önce kopyaladığınız satınalma siparişinde halihazırda var olan tüm satınalma siparişi satırlarını siler. Uyarı vermeden mevcut tüm satırları sildiğinden bu seçeneği dikkatli kullanın.  
    - **Sipariş başlığını kopyala** seçeneğini kullanırsanız yeni siparişinizde başlık bilgilerini el ile oluşturmanız gerekmez. Bu seçeneğin satıcıyla ilişkili alanlar için varsayılan değerlerin kullanılmasına neden olacağını unutmayın. Kopyalama yaptığınız belgede kopyalamak istediğiniz varsayılan olmayan değerler varsa **Tam olarak kopyala** seçeneği de kullanın.   
    - Kopyalama yapabileceğiniz farklı belge kaynakları vardır ve her biri bu sayfa üzerinde ayrı bir bölüme sahiptir. Örneğin, **Satın alma siparişleri** bölümü mevcut satınalma siparişlerinden kopyalama yapmanızı sağlar.  

8. **Satınalma siparişleri** bölümünde, panonuza kopyalanmasını istediğiniz satırları seçin. Diğer satınalma siparişlerinden ek satınalma siparişi satırlarının seçilmesi ve bunların siparişinize kopyalanması mümkündür. Satınalma belgelerinin diğer türlerinden de satır eklemek mümkündür. Sonraki birkaç adımda farklı seçenekler gözden geçirilir.  
9. **Onay** bölümünü genişletin. Kopyalama kaynağı olarak kullanmak için satınalma siparişi onaylarını buradan seçebilirsiniz. Satınalma siparişi onayları ilişkili satınalma günlüğü kimliği veya satınalma siparişi kimliği ile tanımlanır.  
10. **Ürün girişleri** bölümünü genişletin. Kopyalama kaynağı olarak kullanmak için ürün girişi günlüklerini buradan seçebilirsiniz. Ürün girişi günlükleri ürün giriş fişi veya satınalma siparişi kimliği ile tanımlanır.   
11. **Faturalar** bölümünü genişletin. Kopyalama kaynağı olarak kullanmak için satıcı faturalarını buradan seçebilirsiniz. Faturalar, fatura fişi veya satınalma siparişi kimliğiyle tanımlanır.   
12. **Seçilen satırlar veya kopyalanacak başlık** bölümünü genişletin. Bu görünüm siparişinize kopyalamak için seçilmiş tüm belgeler ve satırların özetini gösterir.   
13. **Tamam**'ı seçin. Seçtiğiniz satır yeni satınalma siparişinize kopyalandı.   

## <a name="copy-lines-to-an-existing-purchase-order"></a>Satırları mevcut satınalma siparişine kopyalayın  

Siparişin tamamını kopyalamak yerine yeni bir PO oluşturmak, PO başlığındaki bilgileri tamamlamak ve sonra mevcut siparişlerden tek tek satırları kopyalamak daha yaygın bir uygulamadır.  

1. **Satın alma siparişi** satırını seçin.
2. **Tümünden**'i seçin. Sayfa önceden görüntülenenin aynısını açar ancak sipariş satırlarını görünümünden açıldığında farklı seçenekler seçilir. Parametreleri gözden geçirelim.   
3. **Parametreler** bölümünü genişletin.

    - **Satınalma satırlarını sil** seçeneği seçilmez. Bu, mevcut satırları kaldırmadan siparişinize yeni satırlar kopyalayabileceğiniz anlamına gelir.   
    - Siparişe yalnızca ek satırlar eklediğimizden **Sipariş başlığını kopyala** seçeneği de seçilmez.   
    - Bu örnekte, mevcut satınalma siparişinden satırları kopyalayacağız.   

4. İstenen satınalma emri için satırı seçin. Bu PO üzerinde tek sipariş satırının da seçildiğine dikkat edin.  
5. **Tamam**'ı seçin. Ek sipariş satırı satınalma siparişinize eklendi.  

