---
title: Dengeleme mali boyutlarını nasıl ayarlayabilirim?
description: Bu konuda, Dengeleme mali boyutu özelliğini ayarlama ve kullanma seçenekleri açıklanmaktadır.
author: kweekley
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-08-17
ms.dyn365.ops.version: 10.0.210
ms.openlocfilehash: 188c15c4cb0c295a9fcbb08273ddb391fbc29e24
ms.sourcegitcommit: b4c78655f2ab4b0e7ead96dfb9cf087a18014253
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2021
ms.locfileid: "7468952"
---
# <a name="how-do-i-set-up-balancing-financial-dimensions"></a>Dengeleme mali boyutlarını nasıl ayarlayabilirim?

[!include [banner](../includes/banner.md)]

Bu konuda, Dengeleme mali boyutu özelliğini ayarlama ve kullanma seçenekleri açıklanmaktadır.

## <a name="symptom"></a>Belirti

Dengeleme mali boyutlarını ayarlamak için iki seçenek vardır. İlk seçenek, **Genel muhasebe** kurulumu sayfasındaki **Dengeleme mali boyutu** alanını kullanmaktır (**Genel muhasebe \> Genel muhasebe kurulumu \> Kayıt defteri**). İkinci seçenek, **Mali boyutlar** sayfasındaki **Boyutun dengelenmesi gerekir** alanını kullanmaktır (**Genel muhasebe > Hesap planı \> Boyutlar \> Mali boyutlar**). Bu konuda, bu iki seçenek arasındaki fark açıklanmaktadır.

## <a name="resolution"></a>Çözüm

Kuruluşlar, genellikle mali boyut düzeyinde dengede olan bir bilanço oluşturmak için dengeleme boyutlarını kullanır. Her iki özelliğin de etkinleştirilmesi, deftere nakledilen, dengeli olmayan boyutları dengeye getirmeyecektir. Her iki özelliği de etkinleştirmeden önce bilançoyu dengeye getirmek için ilk olarak ayarlama girişlerini el ile girmelisiniz.

Bu iki seçenek birbirini dışlar. Kuruluşunuzun kullandığı seçenek, iş gereksinimlerinizi temel almalıdır. Hem genel muhasebe kurulumunda hem de mali boyut kurulumunda dengeleme boyutunu tanımlayan ve ardından gerekli olan ek kurulumun bir kısmını veya tamamını tamamlayan müşteriler olduğunu sıkça duyuyoruz. Ancak mali boyut düzeyindeki bir dengesizlik nedeniyle yine de deftere nakledemezler.

Aşağıdaki bölümlerde iki seçenek tanımlanmakta ve bunların nasıl ayarlanacağı açıklanmaktadır.

### <a name="ledger--balancing-financial-dimension"></a>Genel muhasebe: Dengeleme mali boyutu

**Genel muhasebe** kurulumu sayfasındaki dengeleme boyutu, birimlerarası muhasebeyi etkinleştirmek için kullanılır. İşlevi açmak için şu adımları izleyin.

1. Hangi mali boyutun dengeleme boyutu olacağını belirleyin.

    - Bu işlev, dengeleme boyutu olarak yalnızca bir mali boyut seçmenize olanak tanır.
    - **Genel muhasebe** kurulumu sayfasında boyutu şimdilik seçmeyin.
    - Bilançonuzun seçilen mali boyut için zaten dengeli olduğundan emin olun.

2. Dengeleme mali boyutu için hesap yapısını güncelleştirin.

    - Dengeleme mali boyutu, kayıt defterine atanan tüm hesap yapılarına dahil edilmelidir.
    - Mali boyut, hesap yapısında boşluklara izin vermemelidir. Bu kısıtlama, Genel muhasebe defterine nakledilen her muhasebe girişinin mali boyut değeri içermesini sağlar. Dengeleme boyutları kullanıldığında boş boyutlar geçerli değildir.

3. **Otomatik hareketler için hesaplar** sayfasında (**Genel muhasebe \> Deftere nakil ayarı \> Otomatik hareketler için hesap**), birimlerarası borç ve alacak ana hesaplarını tanımlayın.
4. **Genel muhasebe** kurulumu sayfasında (**Genel muhasebe \> Genel muhasebe kurulumu \> Kayıt defteri**), **Dengeleme mali boyutu** alanında, dengeleme için kullanılacak bir mali boyut seçin.

Hareketler girilip deftere nakledilirken seçilen mali boyut dengelenmezse sistem, deftere nakil sırasında muhasebe girişini dengelemek için gereken borç veya alacak girişlerini otomatik olarak ekler. Birimlerarası işlem için borç ve alacak defteri hesapları, Genel muhasebede nakledilen fişte gösterilir. Ancak muhasebe girişlerinin deftere nakledildiği günlüklerde veya kaynak belgelerde gösterilmezler.

### <a name="financial-dimensions--require-the-dimension-to-be-balanced"></a>Mali boyutlar: Boyutun dengelenmesi gerekir

**Mali boyutlar** sayfasındaki dengeleme boyutu genellikle kamu sektörü şirketleri tarafından kullanılsa da işlev herhangi bir kamu sektörü yapılandırma anahtarına bağlı değildir. Sistemde herhangi bir sınırlama olmadığı için kuruluşunuz kamu sektörü kuruluşu olmasa da bu işlevi kullanabilirsiniz.

Bu işlev, her işlemi otomatik olarak dengelemek için deftere nakil tanımlarının kullanılmasını gerektirdiğinden, genellikle kamu sektörü müşteri tabanında kullanılır. **Otomatik hareketler için hesaplar** sayfasında tanımlanan birimlerarası borç ve alacak hesaplarını, muhasebe girişlerini otomatik olarak dengelemek için kullanmaz. Deftere nakil tanımları uygulandıktan sonra boyut düzeyinde bir muhasebe girişi dengelenmezse birimlerarası borç ve alacak hesapları tanımlansa bile hareket deftere nakledilmez.

Hem genel muhasebe kurulumunda hem de finansal boyut kurulumunda dengeleme boyutunu tanımlayan müşteriler olduğunu sıkça duyuyoruz. Bu durumda, sistem mali boyutlar işlevini kullanır. Mali boyut düzeyinde boyut dengeleme kurulumu, deftere nakil sırasında önceliklidir. Deftere nakil tanımı, mali boyut düzeyinde dengeli bir muhasebe girişi oluşturmazsa deftere nakil başarısız olur.

Mali boyut düzeyinde bir dengeleme boyutunun kullanımını etkinleştirmek için şu adımları izleyin.

1. Hangi mali boyutların dengeleme boyutları olacağını belirleyin.

    - Dengeleme boyutu olarak birden fazla mali boyut ayarlayabilirsiniz.
    - **Mali boyutlar** sayfasında bir hareketi dengelemede gerekli olacak mali boyutları şimdilik ayarlamayın.

2. Kuruluşunuz tarafından kullanılan her günlük veya kaynak belgesi türü için deftere nakil tanımlarını tanımlayın. Deftere nakil tanımı, deftere nakledilmemiş bir günlük veya kaynak belgesindeki genel muhasebe hesaplarını "eşleşme ölçütü" olarak kullanır. Deftere nakil tanımı daha sonra muhasebe girişi haline gelen "oluşturulan girişleri" döndürür. Deftere nakil tanımı doğru ayarlanmışsa oluşturulan giriş, eşleşme ölçütü genel muhasebe hesaplarını ve ayrıca boyut düzeyinde muhasebe girişini dengelemek için ek hesapları içerir. Daha fazla bilgi için bkz. [Deftere nakil tanımları](posting-definitions.md). 
   
   Deftere nakil tanımı her hareket türünde desteklenmez. Örneğin, deftere nakil tanımları Genel günlük veya Sabit kıymet günlüğü aracılığıyla girilen hiçbir hareket için tanımlanamaz. Günlük kaydı veya kaynak belgesi için kayıt tanımı tanımlanamıyorsa hareketin mali boyut değerinde el ile dengelenmesi gerekir. Örneğin, genel bir günlük girişi yapılırsa ve dengeleme boyutu Departman boyutuysa her departman değerinin dengede olduğundan emin olmalısınız.  Boyut, her departman değeri için dengelenmemişse fişe el ile birimlerarası borç veya alacak eklenerek dengesizlik düzeltilene kadar fiş deftere nakledilmez. 

    > [!IMPORTANT]
    > Çok fazla sayıda hareketin el ile dengelenmesi gerekiyorsa **Mali boyutlar** sayfasındaki dengeleme boyutu işlevini **kullanmamalısınız**. Bunun yerine, **Genel muhasebe** kurulumu sayfasındaki dengeleme boyutu işlevini kullanın.

3. Deftere nakil tanımları tanımlandıktan sonra, mali boyutlar dengeleme için gerekli olarak işaretlenebilir.

Hareketleri girip deftere naklederken, muhasebe girişlerini belirlemek için nakil sırasında deftere nakil tanımları çağrılır. Mali boyutlar dengeliyse muhasebe girişleri belirlendikten sonra doğrulama gerçekleşir. Mali boyutlar dengeli değilse hareket deftere nakledilemez ve borçların belirli bir boyut için alacaklara eşit olmadığını bildiren bir ileti alırsınız.
