---
title: Satınalma iade siparişi oluşturma
description: Bu yordam, bir satıcı fatura belgesinden satırları yeni bir satınalma siparişine kopyalamak için Alacak dekontu eylemini kullanarak bir satın alma iade siparişini nasıl oluşturacağınızı gösterir.
author: RichardLuan
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, PurchCopying, InventMarking, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10b3e695ffcd44909be4781eac5d4eaeef199b03
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017071"
---
# <a name="create-a-purchase-return-order"></a>Satınalma iade siparişi oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordam, bir satıcı fatura belgesinden satırları yeni bir satınalma siparişine kopyalamak için Alacak dekontu eylemini kullanarak bir satın alma iade siparişini nasıl oluşturacağınızı gösterir. Ayrıca siparişi nasıl onaylayacağınızı ve malların satıcıya geri sevkiyatını nasıl işleyeceğinizi gösterir. Bu yordamda gösterilen örnek, demo verileri şirketi USMF'de kullanılabilir. Bu görev genellikle bir satınalma temsilcisi tarafından gerçekleştirilir.

## <a name="create-a-new-purchase-return-order"></a>Yeni bir satın alma iade siparişi oluşturun
1. **Gezinti bölmesi > Modüller > Tedarik ve kaynak atama > Satınalma siparişleri > Tüm satınalma siparişleri** öğesine gidin. İlk adım satınalma iade siparişi olarak kullanılacak yeni bir satınalma siparişi oluşturmaktır.  
2. **Yeni**'ye tıklayın.
3. **Satıcı hesabı** alanına "US-102" girin.
4. **Tamam**'a tıklayın.
5. **Eylem Bölmesi**'nde, **Satınalma** öğesine tıklayın.
6. **Alacak dekontu**'na tıklayın. Bu sayfadan mevcut satıcı faturasını iade siparişinize kopyalayabilirsiniz. Bu, diğer kopyalama eylemleri için kullanılanla aynı sayfadır. Ancak Alacak dekontu eyleminden açıldığından sayfa, satıcı faturalarını mahsuplaştıran bir iade siparişinin oluşturulmasını desteklemek üzere yapılandırılır.  
7. **Parametreler** bölümünü genişletin.
    - **İşareti tersine çevir** seçeneği otomatik olarak seçilir ve değiştirilemez. Bu, işaretin miktarlar için değiştirilmesini ve eklenen sipariş satırlarının satıcı faturasını mahsuplaştırmasını sağlar.  
    - **Masrafları kopyala** seçeneği otomatik olarak seçilir ve değiştirilemez. Başka bir deyişle satıcı faturasındaki masraflar orijinal masrafı mahsuplaştırmak için satınalma iade siparişine eklenir. Sipariş başlığı ve satırları üzerindeki değişiklikleri daha sonra değiştirmek mümkündür.  
    - **Tam olarak kopyala** seçeneği otomatik olarak seçilir ve değiştirilemez. Bu, satıcı faturası başlığı ve satırlarında tüm alanlardaki değerlerin tam olarak kopyalanmasını sağlar. Başka bir deyişle, satınalma iade siparişi satıcı fatura belgesinde kullanılan tüm koşullarla eşleşen değerlerle oluşturulur. 
    - **Satınalma satırlarını sil** seçeneği, yeni satırları eklemeden önce satınalma siparişinde halihazırda mevcut tüm satınalma siparişi satırlarını siler. Bu örnekte satınalma iade siparişine henüz satır eklenmediğinden herhangi bir etki mevcut değildir. Uyarı vermeden mevcut tüm satırları sildiğinden bu seçeneği dikkatli kullanın.  
    * **Sipariş başlığını kopyala** seçeneği otomatik olarak seçilir ve değiştirilemez. Bu, bilgilerin satıcı faturasından kopyalanmasını ve satınalma iade siparişi başlığına uygulanmasını sağlar. Satınalma iade siparişinin benzer koşulları kullanarak faturayı mahsuplaştırmasını sağladığı için bu faydalıdır.  
8. **Parametreler** bölümünü daraltın.
9. **Faturalar** bölümünü genişletin. Sayfa, Alacak dekontu eyleminden açıldığından kullanılabilir tek seçenek bilgileri satıcı faturasından kopyalamaktır. Bu sekme önceden oluşturduğunuz satınalma iade siparişinde belirtilen satıcı hesabı için tüm kullanılabilir faturaları gösterir.   Faturalar, fatura fişi veya satınalma siparişi kimlikleriyle tanımlanır.
10. Fatura numarası AP-0006 ile tanımlanan satıcı faturasını konumlandırın ve bu satırda olan herhangi bir alana tıklayarak bu satırı vurgulayın.
11. Satır için onay kutusuna tıklayarak satırı seçin. Bu satıcı faturasındaki kullanılabilir satırların siparişle birlikte otomatik olarak seçildiğine dikkat edin. Bu satıcı faturası 2 sipariş satırına sahiptir. Bu örnekte ikinci satırdaki miktarın bir kısmı iade edilecektir.
12. İkinci satırı (M0006 maddesi olanı) bu satırdaki herhangi bir alana tıklayarak vurgulayın.
13. **Miktar** alanında, miktarı 10 olarak değiştirin. Bu, satıcıya iade edeceğimiz miktardır. 
14. İlk satırı (M0005 maddesi olanı) bu satırdaki herhangi bir alana tıklayarak vurgulayın.
15. Satır için onay kutusunun işaretini kaldırın. Yalnızca seçtiğiniz satırlar siparişinize kopyalanır.
16. **Faturalar** bölümünü daraltın.
17. **Seçilen satırlar veya kopyalanacak başlık** bölümünü genişletin. Bu görünüm, siparişinize kopyalanması için seçtiğiniz tüm belgelerin ve satırların bir özetini gösterir.  
18. **Seçilen satırlar veya kopyalanacak başlık bölümünü** daraltın.
19. **Tamam**'a tıklayın. Seçmiş olduğunuz satır şimdi satın alma iade siparişinize kopyalandı. **Miktar** alanı -10 gösterir.   
20. **Satınalma siparişi satırı** bölümünde, **Stok** öğesine tıklayın.
21. **İşaretleme**'ye tıklayın. Oluşturulan sipariş satırı satıcı faturasındaki stok işlemine göre işaretlenmiştir. Bu, satıcıya iade edilen stok ile daha önce alınmış olan stokun aynı olduğunu garantiye alır. Örneğin, stokun Tüketildi olarak işaretlenmiş olduğu veya ürünün işaretleme kullanmayan bir ürün olması gibi işaretlemenin olmadığı bazı durumlar vardır.  

22. **Tamam**'a tıklayın.

## <a name="confirm-and-record-the-shipment-of-goods"></a>Malların sevkiyatını onaylayın ve kaydedin
1. **Eylemler > Onayla**'yı tıklayın.
2. **Eylem Bölmesinde**, **Teslim al** öğesine tıklayın.
3. **Ürün girişi** öğesine tıklayın.
    - Bu sayfa satınalma siparişleri için ürün girişlerini kaydetmek ve ayrıca malların satıcıya iadesini işlemek için kullanılır. Eksi değerli miktarı olan sipariş satırları malların satıcıya iade edildiği anlamına gelir ve bu sayfadan oluşturulabilen belge bu amaçla sevk irsaliyesi olarak kullanılabilir.   
    - Bu örnek için **Miktar** alanında Sipariş edilen miktarı seçin. Bu işlem, sipariş satırlarının oluşturulduğu tam sipariş miktarı için sevkiyatın işleneceğini garantiye alır.   
4. **Ürün girişi** alanına bir değer girin. Bu alan, ürün giriş günlüğünde makbuz olarak kullanılacak bir referans girmek için kullanılır.  
5. **Tamam**'a tıklayın. Mallar şimdi satın alma iade siparişinde sevk edildi olarak kaydedilmiştir ve bir ürün giriş yevmiye defteri oluşturulmuştur. Satınalma siparişiyle oluşturulan günlükleri gözden geçirmek ve nelerin ve ne zaman alındığını veya iade edildiğini görmek için Ürün girişi etkinliğini kullanabilirsiniz.  

