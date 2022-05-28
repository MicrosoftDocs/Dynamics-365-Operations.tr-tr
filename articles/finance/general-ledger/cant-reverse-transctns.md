---
title: Bu hareketi neden tersine çeviremiyorum?
description: Bu konuda, hareketlerin tersine çevrilememesinin farklı nedenleri açıklanmaktadır. Ayrıca bu soruna yönelik çözümler listelenmektedir.
author: kweekley
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-07-21
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e18caf1dbdf8191713c17b1793f5da44cf2f182b
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724543"
---
# <a name="why-cant-i-reverse-this-transaction"></a>Bu hareketi neden tersine çeviremiyorum?

[!include [banner](../includes/banner.md)]

Bu konuda, hareketlerin tersine çevrilememesinin farklı nedenleri açıklanmaktadır. Ayrıca bu soruna yönelik çözümler listelenmektedir.

## <a name="symptom"></a>Belirti

Kuruluşlar, deftere naklettikleri bir hareketi tersine çevirmeleri gereken durumlarla karşılaşabilir. Bazen sistem, kuruluşların bu hareketleri tersine çevirmelerini engeller. Bu davranış iki farklı soruyu gündeme getirebilir:

- Bu hareketi neden tersine çeviremiyorum?
- Toplu ters işlem özelliği bu davranışı nasıl etkiler?

## <a name="resolution"></a>Çözüm

Hareketler, tersine çevrilebilmeleri için belirli ölçütleri karşılamalıdır. Bu konunun geri kalan bölümleri her modül için doğrulama sağlar. Bu konu, Microsoft Dynamics 365 Finance uygulamasındaki hareketlere odaklansa da bazı kavramlar ve doğrulama yöntemleri, Dynamics 365 Supply Chain Management gibi diğer uygulamalara da uygulanabilir.

Ek olarak, bir hareketin tersine çevrildiği yer, tersine çevrilip çevrilemeyeceğini etkileyebilir. Örneğin, çek olarak deftere nakledilen bir satıcı ödemesi yalnızca banka hesapları için hareket sayfasındaki **Çekler** bölümünden tersine çevrilebilir. Genel muhasebedeki **Fiş hareketleri** sayfasından tersine çevrilemez.

**Özellik yönetimi** çalışma alanındaki **Birden çok belgeyi toplu tersine çevirme** (Toplu ters işlem özelliği olarak da bilinir) özelliğinin açılması kaç hareketin tersine çevrilebileceğini ve nerede tersine çevrilebileceklerini etkiler. Bu özelliğin açılması iki avantaj sağlar:

- Bazı hareket türlerinde aynı anda birden fazla hareket, deftere nakledildikleri günlükten veya **Fiş hareketleri** sayfasından seçilerek tersine çevrilebilir. Ancak özellik etkinleştirilmeden önce hareketlerin hepsinin tersine çevrilebilir olması gerekir. Bu özellik kullanılmaya başlamadan önce hareketlerin tek tek tersine çevrilmesi gerekiyordu.
- *Bazı* yardımcı defter hareketleri, günlükten (yevmiye defteri) veya **Fiş hareketleri** sayfasından tersine çevrilebilir. Yardımcı defter sayfasından tersine çevrilmeleri gerekmez. Örneğin, bir satıcı faturası günlüğü önceden yalnızca **Satıcı hareketleri** sayfasından tersine çevrilebilirdi. Ancak artık Genel muhasebe tarafındaki günlükten veya **Fiş hareketleri** sayfasından da tersine çevrilebilir. Bu konudaki her bir bölüm bu avantajın geçerli olmadığı hareket türlerini açıklamaktadır.

Toplu ters işlem özelliği, tersine çevrilecek daha fazla türdeki hareketin tersine çevrilmesine olanak **sağlamaz**. Hareket türü, özellik açılmadan önce tersine çevrilemiyorsa özellik açıldıktan sonra da tersine çevrilemez. Örneğin, satınalma siparişi satıcı faturaları, Toplu ters işlem özelliğinin açık olup olmadığından bağımsız olarak tersine çevrilemez.

Toplu ters işlem özelliği hakkında daha fazla bilgi için bkz. [Günlüğe nakli tersine çevirme](reverse-journal-posting.md).

## <a name="general-ledger"></a>Genel muhasebe

Genel muhasebe düzeltmeleri yalnızca genel muhasebe hesapları kullanılarak girilir. Bu nedenle, yalnızca Genel muhasebeyi güncelleştirirler.

Toplu ters işlem özelliği kapatılırsa genel muhasebe düzenlemelerinin çoğu genel muhasebenin **\<main account\> hareketleri** sayfasından tek tek tersine çevrilebilir (**LedgerTransAccount**). (Sayfanın tam başlığı, seçilen ana hesaba göre değişir.) Sayfa, ana hesap defterine nakledilen tüm hareketleri gösterir. Genellikle **Mizan listesi** sayfasından veya **Fiş hareketleri** sayfasındaki **Hareketler** seçilerek açılır.

Toplu ters işlem özelliği açılırsa bir veya daha fazla genel muhasebe fişi artık **Fiş hareketleri** sayfasından ve hareketin deftere nakledildiği günlükten tersine çevrilebilir. Genel muhasebe yabancı para birimi yeniden değerleme işlemi, konsolidasyon ve yıl sonu kapanışı hareketleri özel durumlardır. Bu hareketler, yıl sonu kapanışının yapıldığı sayfalardan tersine çevrilir.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Hareketlerin tersine çevrilememelerinin nedenleri

Hareketler aşağıdaki nedenlerle tersine çevrilemez:

- Yevmiye defteri:

    - Mali dönem beklemede veya kalıcı olarak kapalı:

        - Tersine çevirme tarihi açık olmayan bir mali dönemdeyse hareket tersine çevrilemez.
        - Hareket, bir ters işlem tarihinin girişini destekliyorsa ters işlem tarihi açık bir mali döneme değiştirilerek hareket yine de tersine çevrilebilir.

    - Yıl sonu kapanışı işlemi çalıştırıldı:

        - Hareketin muhasebe tarihi, yıl sonu kapanışı işleminin gerçekleştiği bir mali yıl içindedir. Mali yıldaki bir dönem hala açık olsa da mali yıl için yıl sonu kapanışı işlemi çalıştırılmışsa hareket tersine çevrilemez. Mali yıl, içindeki dönemlerden farklı bir duruma sahiptir.
        - Yıl sonu kapanışı tersine çevrilebilir ve ardından hareket tersine çevrilebilir. Bu yaklaşım bir seçenek olmayabilir. Mali kapanış işleminin durumuna bağlı olarak kapatılan mali yılın veya sonraki mali yılın açık döneminde bir tersine çevirme hareketini el ile girmek daha kolay olabilir. Yıl sonu kapanışı işleminden geçen mali yılın açık dönemine yeni bir hareket deftere nakledilirse yıl sonu kapanışının yeniden çalıştırılması gerekir.

    - Hareket ters işlemi zaten devam ediyor:

        - Hareket, tersine çevirme işlemindeyse bu işlemin tamamlanması gerekir. Ayrı bir ters işlem yapılamaz. 
        - Ters işlem tamamlandıktan sonra tersine çevrilen bir hareket tekrar tersine çevrilebilir (yani, ters işlem tersine çevrilebilir).

    - Genel muhasebe hesabı kapatması:

        - Hareketin bir veya daha fazla satırı **Genel muhasebe hesabı kapatmaları** periyodik görevi (**Genel muhasebe \> Periyodik görevler \> Genel muhasebe hesabı kapatmaları**) kullanılarak kaydın LedgerTransSettlement tablosunda yer alması için genel muhasebe hesabı kapatması işlemine tabi tutulmuşsa hareket tersine çevrilemez.
        - Genel muhasebe hesabı kapatması tersine çevrilebilir ve ardından fiş tersine çevrilebilir.

    - Şirketlerarası:

        - Hareket, bir şirketlerarası hareket ise tersine çevrilemez.
        - Hareket, şirketlerarası bir hareket **değildir** ancak **Şirketlerarası kurulum** sayfasında tanımlanan bir "vade sonu" veya "vade başlangıcı" ana hesabına nakledilmiştir.

    - Tahakkuklar:

        - Tahakkuk eden genel muhasebe fişi tersine çevrilirse tahakkuk eden giriş ve ilgili tüm tahakkuk alt hareketleri tersine çevrilir.
        - Tahakkuk alt hareketleri tek tek tersine çevrilemez.

- Gelir kabulü günlüğü:

    - Gelir kabulü hareketleri tersine çevrilemez.
    - Gelir, gelir kabulü günlüğü aracılığıyla muhasebeleştirildiğinde fiş yalnızca genel muhasebe hesaplarına nakledilir. Bu nedenle, **Fiş hareketleri** gibi sayfalarda hareketler yalnızca genel muhasebe girişleri gibi görünür.

- Yabancı para birimi yeniden değerleme işlemi:

    - Yabancı para birimi yeniden değerleme hareketleri yalnızca yeniden değerlemenin çalıştırıldığı Genel muhasebe **Yabancı para birimi yeniden değerleme** sayfasından tersine çevrilebilir.
    - Ters işlem yalnızca açık bir mali döneme nakledilirse tamamlanabilir.

- Konsolidasyon:

    - Konsolidasyon hareketleri yalnızca **Konsolidasyon hareketleri** sayfasından tersine çevrilebilir.
    - Ters işlem yalnızca açık bir mali döneme nakledilirse tamamlanabilir.

- Yıl sonu kapanışı:

    - Yıl sonu kapanışı hareketleri (hem kapanış hem de açılış hareketleri) şu şekillerde tersine çevrilebilir:

        - Genel muhasebe yıl sonu kapanışı iyileştirmeleri özelliği kapatılırsa **Yıl sonu kapanışı** iletişim kutusunda **Önceki kapanışı geri al** seçeneğini belirleyin.
        - Genel muhasebe yıl sonu iyileştirmeleri özelliği açılırsa **Yıl sonu kapanışı** sayfasında yıl sonu kapanışı için oluşturulan şirket ve mali yıl kayıtlarını seçin ve ardından **Yıl sonu kapanışını tersine çevir** seçeneğini belirleyin.

    - Yıl sonu kapanışının tersine çevrilmesinin aslında kapanış ve açılış hareketlerini sildiğini unutmayın. Ters kayıt fişi asla deftere nakledilmez.

## <a name="accounts-payable"></a>Borç hesapları

Birden çok hareket türü Borç hesapları yardımcı defterini güncelleştirir. Satıcı faturaları, satıcı faturası günlükleri ve gider raporları örnek olarak verilebilir.

Toplu ters işlem özelliği kapatılırsa faturalar için **Satıcı hareketleri** sayfasından veya çek ödemeleri için **Banka hesabı** sayfasından hareketler tek tek tersine çevrilebilir.

Toplu ters işlem özelliği açılırsa bir veya daha fazla Borç hesabı hareketi, **Fiş hareketleri** sayfasından ve hareketlerin deftere nakledildiği günlükten de tersine çevrilebilir. Ancak satıcı ödemeleri yine de yalnızca banka hesabından tersine çevrilebilir. Ayrıca satıcı hareketleri, kayıt defterinin **\<main account\> hareketleri** sayfasından tersine çevrilemez. Yalnızca **Fiş hareketleri** sayfasından tersine çevrilebilirler.

Bazı hareketlerin hiçbir zaman tersine çevrilemeyeceğini unutmayın. Satınalma siparişi, satıcı faturaları ve elektronik satıcı ödemeleri örnek olarak verilebilir.

### <a name="reasons-why-vouchers-cant-be-reversed"></a>Fişlerin tersine çevrilememelerinin nedenleri

Fişler aşağıdaki nedenlerle tersine çevrilemez:

- Mali dönem beklemede veya kapalı:

    - Tersine çevirme tarihi açık olmayan bir mali dönemdeyse hareket tersine çevrilemez.
    - Hareket, bir ters işlem tarihinin girişini destekliyorsa ters işlem tarihi açık bir mali döneme değiştirilerek hareket yine de tersine çevrilebilir.

- Genel muhasebe yıl sonu kapanışı işlemi çalıştırıldı:

    - Hareketin muhasebe tarihi, Genel muhasebede kapatılan bir mali yıl içindedir. Mali yıldaki bir dönem hala açık olsa da mali yıl için yıl sonu kapanışı işlemi çalıştırılmışsa hareket tersine çevrilemez. Mali yıl, içindeki dönemlerden farklı bir duruma sahiptir.
    - Yıl sonu kapanışı tersine çevrilebilir ve ardından hareket tersine çevrilebilir. Bu yaklaşım bir seçenek olmayabilir. Mali kapanış işleminin durumuna bağlı olarak kapatılan mali yılın veya sonraki mali yılın açık döneminde bir tersine çevirme hareketini el ile girmek daha kolay olabilir. Yıl sonu kapanışı işleminden geçen mali yılın açık dönemine yeni bir hareket deftere nakledilirse yıl sonu kapanışının yeniden çalıştırılması gerekir.

- Yardımcı defter günlüğü girişi Genel muhasebeye aktarılmadı:

    - Bu neden yalnızca satınalma harici satıcı faturaları için geçerlidir.
    - Girişi Genel muhasebeye aktarmak için **Henüz transfer edilmemiş alt muhasebe günlük girişleri** sayfasını kullanın. Satınalma siparişi olmayan satıcı faturası daha sonra **Satıcı hareketleri** sayfasından tersine çevrilebilir.

- Kapatma:

    - Hareket (fatura veya ödeme gibi) kapatılır veya kapatılmak üzere işaretlenir.

        - **Satıcı hareketleri** sayfasındaki **Kapatmaları görüntüle** veya **Kapatma \> Kapatma geçmişi**'ni seçerek bir hareketin kapatıldığını ya da kapatma için işaretlendiğini doğrulayabilirsiniz.
        - Ayrıca hareketlerden birinin tersine çevrilmesi gerekiyorsa bir kapatmayı **Satıcı hareketleri** sayfasından (**Kapatma \> Kapatmayı geri al**) tersine çevirebilirsiniz.

- Fiş, aynı fiş numarası kullanılarak girilen birden fazla yardımcı defter hareketi içeriyor (Bir fiş sorunu).
- Fatura onaylanmadı:

    - Faturada **Onay** kutusu işaretlenmemişse fatura tersine çevrilemez.

        - Bu durumda onay, iş akışı sürecindeki onaylara değil faturadaki **Onay** seçeneğine başvurur. Bu seçenek, bir faturanın ödenmesini önlemek için kullanılır. Genellikle satıcı faturası kayıt faturaları için kullanılır.

- Hareket, fatura havuzunda:

    - Havuzdaki bir fatura doğrudan **Satıcı hareketleri** sayfasından tersine çevrilemez. Bunun yerine, **Fatura onay günlüğü** sayfasındaki iptal işlemi aracılığıyla tersine çevrilmelidir.

- Hareketin düzeltilmiş bir üst faturası var (Hintçe yerelleştirmesi).
- Hareket, **Havale edilen fatura** şeklinde bir senet durumuna sahiptir.
- Hareket, kısmi vergi kapatması için kullanılır.
- Hareket bir satıcı hesabı içeriyor ancak **\<main account\> hareketleri** sayfası gibi yanlış bir sayfadan tersine çevriliyor:

    - Bu nedenden de anlaşılacağı gibi Toplu ters işlem özelliği açıkken bile bazı yardımcı defter hareketleri yalnızca belirli sayfalardan tersine çevrilebilir.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Tersine çevrilemeyen hareket türleri

Aşağıdaki hareket türleri tersine çevrilemez:

- Yabancı para birimi yeniden değerleme işlemi:

    - Genel muhasebe yabancı para birimi yeniden değerleme işleminden farklı olarak Alacak hesapları ve Borç hesapları yabancı para birimi yeniden değerleme işlemleri tersine çevrilemez. Bunun yerine, yeniden değerleme fatura tarihi kullanılarak yeniden çalıştırılmalıdır. Bu durumda yeniden değerleme, fatura tarihindeki döviz kurunu kullanır ve esasen gerçekleşmemiş kazanç veya kaybı 0'a (sıfır) getirir. Bu nedenle sonuç, önceki yeniden değerleme işleminin tersine çevrilmesinin sonucuna benzer. Ancak fatura üzerindeki varsayılan döviz kuru değiştirilirse aynı tutarın tersine çevrilmeyeceğini unutmayın.

- Satınalma siparişi satıcı faturası:

    - Satıcı faturasını tersine çevirmek için bir alacak dekontu oluşturulmalıdır. Ters kaydedilen hareketin nasıl oluşturulacağı hakkında daha fazla bilgi için bkz. [Satınalma iade emri oluşturma](../../supply-chain/procurement/tasks/create-purchase-return-order.md).

- Senet
- İhracat sevkiyatı banka kredi mektubu

## <a name="accounts-receivable"></a>Alacak hesapları

Birkaç hareket türü Alacak hesapları yardımcı defterlerini güncelleştirir. Satış siparişlerinden gelen müşteri faturaları, yevmiye defteri üzerinden girilen müşteri faturaları, serbest metin faturaları, müşteri ödemeleri ve gider yazmalar örnek olarak verilebilir.

Toplu ters işlem özelliği kapatılırsa faturalar için **Müşteri hareketleri** sayfasından veya havaleler için **Banka hesapları** sayfasından hareketler tek tek tersine çevrilebilir. Ödemenin nasıl tersine çevrileceği hakkında bilgi için bu konunun ilerleyen kısımlarındaki [Nakit ve banka yönetimi](cant-reverse-transctns.md#cash-and-bank-management) bölümüne bakın.

Toplu ters işlem özelliği açılırsa bir veya daha fazla Alacak hesabı hareketi, **Fiş hareketleri** sayfasından ve kaydedildikleri günlükten de tersine çevrilebilir. Ancak havaleler yine de yalnızca banka hesabından tersine çevrilebilir ve serbest metin faturaları yalnızca kaynak sayfadan tersine çevrilebilir (düzeltmelere izin veren özellik açıksa). Ek olarak müşteri hareketleri, kayıt defterinin **\<main account\> hareketleri** sayfasından yine de tersine çevrilemez. Ancak **Fiş hareketleri** sayfasından tersine çevrilebilirler.

Bazı hareketlerin tersine çevrilemeyeceğini unutmayın. Satış siparişi, müşteri faturaları ve gider yazmalar örnek olarak verilebilir.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Hareketlerin tersine çevrilememelerinin nedenleri

Hareketler aşağıdaki nedenlerle tersine çevrilemez:

- Mali dönem beklemede veya kalıcı olarak kapalı:

    - Tersine çevirme tarihi açık olmayan bir mali dönemdeyse hareket tersine çevrilemez.
    - Hareket, bir ters işlem tarihinin girişini destekliyorsa ters işlem tarihi açık bir mali döneme değiştirilerek hareket yine de tersine çevrilebilir.

- Genel muhasebe yıl sonu kapanışı işlemi çalıştırıldı:

    - Hareketin muhasebe tarihi, Genel muhasebe yıl sonu kapanışı işleminin gerçekleştiği bir mali yıl içindedir. Mali yıldaki bir dönem hala açık olsa da mali yıl için yıl sonu kapanışı işlemi çalıştırılmışsa hareket tersine çevrilemez. Mali yıl, içindeki dönemlerden farklı bir duruma sahiptir.
    - Yıl sonu kapanışı tersine çevrilebilir ve ardından hareket tersine çevrilebilir. Bu yaklaşım bir seçenek olmayabilir. Mali kapanış işleminin durumuna bağlı olarak kapatılan mali yılın veya sonraki mali yılın açık döneminde bir tersine çevirme hareketini el ile girmek daha kolay olabilir. Yıl sonu kapanışı işleminden geçen mali yılın açık dönemine yeni bir hareket deftere nakledilirse yıl sonu kapanışının yeniden çalıştırılması gerekir.

- Yardımcı defter günlüğü girişi Genel muhasebeye aktarılmadı:

    - Bu neden yalnızca serbest metin faturaları için geçerlidir.
    - Girişi Genel muhasebeye aktarmak için **Henüz transfer edilmemiş alt muhasebe günlük girişleri** sayfasını kullanın. Düzeltme işlevi etkinleştirilirse serbest metin faturası daha sonra tersine çevrilebilir veya düzeltilebilir.

- Kapatma:

    - Hareket (fatura veya ödeme gibi) kapatılır veya kapatılmak üzere işaretlenir.

        - **Müşteri hareketleri** sayfasındaki **Kapatmaları görüntüle** veya **Kapatma \> Kapatma geçmişi**'ni seçerek bir hareketin kapatıldığını ya da kapatma için işaretlendiğini doğrulayabilirsiniz.
        - Ayrıca hareketlerden birinin tersine çevrilmesi gerekiyorsa bir kapatmayı **Müşteri hareketleri** sayfasından (**Kapatma \> Kapatmayı geri al**) tersine çevirebilirsiniz.

- Harekete, aynı fiş numarası kullanılarak girilen birden fazla yardımcı defter hareketi içeriyor (Bir fiş sorunu).
- Fatura onaylanmadı:

    - Faturada **Onay** kutusu işaretlenmemişse fatura tersine çevrilemez.

        - Bu durumda onay, iş akışı sürecindeki onaylara değil fiş satırlarındaki **Onay** seçeneğine başvurur. Bu seçenek, bir faturanın ödenmesini önlemek için kullanılır. Bu seçenek genellikle Borç hesaplarında kullanılmasına rağmen günlükler aracılığıyla girilen Alacak hesapları faturaları için de kullanılabilir.

- Hareketin düzeltilmiş bir üst faturası var (Hintçe yerelleştirmesi).
- Hareket bir müşteri hesabı içeriyor ancak **\<main account\> hareketleri** sayfası gibi yanlış bir sayfadan tersine çevriliyor:

    - Bu nedenden de anlaşılacağı gibi Toplu ters işlem özelliği açıkken bile bazı yardımcı defter hareketleri yalnızca belirli sayfalardan tersine çevrilebilir.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Tersine çevrilemeyen hareket türleri

Aşağıdaki hareket türleri tersine çevrilemez:

- Yabancı para birimi yeniden değerleme işlemi:

    - Genel muhasebe yabancı para birimi yeniden değerleme işleminden farklı olarak Alacak hesapları ve Borç hesapları yabancı para birimi yeniden değerleme işlemleri tersine çevrilemez. Bunun yerine, yeniden değerleme fatura tarihi kullanılarak yeniden çalıştırılmalıdır. Bu durumda yeniden değerleme, fatura tarihindeki döviz kurunu kullanır ve esasen gerçekleşmemiş kazanç veya kaybı 0'a (sıfır) getirir. Bu nedenle sonuç, önceki yeniden değerleme işleminin tersine çevrilmesinin sonucuna benzer. Ancak fatura üzerindeki varsayılan döviz kuru değiştirilirse aynı tutarın tersine çevrilmeyeceğini unutmayın.

- Vergi stopajını ayarlayan bir hareket
- Satış siparişi müşteri faturası:

    - Hareketi tersine çevirmek için bir alacak dekontu veya iade oluşturulmalıdır. Ters kaydedilen hareketin nasıl oluşturulacağı hakkında bilgi için bkz. [Satış iadeleri](../../supply-chain/warehousing/sales-returns.md).

- Kambiyo senedi deftere nakil profili
- Yazar kasa hareketi
- Gelişmiş düzeltme
- Vade farkı dekontu
- Tahsilatlar mektubu
- Banka kredi mektubu
- İhracat sevkiyatı
- Gelir kabulü günlüğü:

    - Gelir kabulü günlüğü aracılığıyla geliri muhasebeleştirdiğinizde fişler genel muhasebe hesaplarına nakledilir. Bu nedenle, yalnızca genel muhasebe girişleri gibi görünürler. Gelir planı, geliri yeniden muhasebeleştirmek için yeniden açılmayacağından bu girişler tersine çevrilemez.

## <a name="cash-and-bank-management"></a>Nakit ve banka yönetimi

Birkaç hareket türü, yevmiye defteri aracılığıyla Banka yardımcı defterini güncelleştirir. Satıcı ödemeleri, müşteri ödemeleri ve banka havaleleri örnekler arasında verilebilir.

Toplu ters işlem özelliği kapatılırsa çekler ve havaleler için **Banka hesapları** sayfasından veya müşteri ödemeleri için **Müşteri hareketleri** sayfasından hareketler tek tek tersine çevrilebilir.

Toplu ters işlem özelliği açılırsa bir veya daha fazla ödeme hareketi, **Fiş hareketleri** sayfasından ve hareketlerin deftere nakledildiği günlükten de tersine çevrilebilir. Ancak havaleler yine de yalnızca banka hesabından tersine çevrilebilir. Ayrıca banka hareketleri, kayıt defterinin **\<main account\> hareketleri** sayfasından yine de tersine çevrilemez. Ancak **Fiş hareketleri** sayfasından tersine çevrilebilirler.

Bazı hareketlerin tersine çevrilemeyeceğini unutmayın. Elektronik satıcı ödemeleri örnek olarak verilebilir.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Hareketlerin tersine çevrilememelerinin nedenleri

Hareketler aşağıdaki nedenlerle tersine çevrilemez:

- Mali dönem beklemede veya kalıcı olarak kapalı:

    - Tersine çevirme tarihi açık olmayan bir mali dönemdeyse hareket tersine çevrilemez.
    - Hareket, bir ters işlem tarihinin girişini destekliyorsa ters işlem tarihi açık bir mali döneme değiştirilerek hareket yine de tersine çevrilebilir.

- Genel muhasebe yıl sonu kapanışı işlemi çalıştırıldı:

    - Hareketin muhasebe tarihi, Genel muhasebe yıl sonu kapanışı işleminin gerçekleştiği bir mali yıl içindedir. Mali yıldaki bir dönem hala açık olsa da mali yıl için yıl sonu kapanışı işlemi çalıştırılmışsa hareket tersine çevrilemez. Mali yıl, içindeki dönemlerden farklı bir duruma sahiptir.
    - Yıl sonu kapanışı tersine çevrilebilir ve ardından hareket tersine çevrilebilir. Bu yaklaşım bir seçenek olmayabilir. Mali kapanış işleminin durumuna bağlı olarak kapatılan mali yılın veya sonraki mali yılın açık döneminde bir tersine çevirme hareketini el ile girmek daha kolay olabilir. Yıl sonu kapanışı işleminden geçen mali yılın açık dönemine yeni bir hareket deftere nakledilirse yıl sonu kapanışının yeniden çalıştırılması gerekir.

- Kapatma:

    - Hareket (ödeme) kapatılır veya kapatılmak üzere işaretlenir.

        - **Satıcı hareketleri** veya **Müşteri hareketleri** sayfasındaki **Kapatmaları görüntüle** ya da **Kapatma \> Kapatma geçmişi**'ni seçerek bir hareketin kapatıldığını veya kapatma için işaretlendiğini doğrulayabilirsiniz.
        - Ayrıca hareketlerden birinin tersine çevrilmesi gerekiyorsa bir kapatmayı **Satıcı hareketleri** veya **Müşteri hareketleri** sayfasından (**Kapatma \> Kapatmayı geri al**) tersine çevirebilirsiniz.

- Harekete, aynı fiş numarası kullanılarak girilen birden fazla yardımcı defter hareketi içeriyor (Bir fiş sorunu).
- Bağlantı hareketleri:

    - Hareket bir bağlantı ödemesiyle ilgiliyse tersine çevrilemez.
    - Bağlantı ödemesinin tersine çevrilmesi gerekiyorsa ödemenin önce bağlantı hesabından bankaya mahsup edilmesi gerekir. Diğer doğrulama kriterlerini karşılaması koşuluyla ödeme daha sonra tersine çevrilebilir.

- Hareket bir banka hesabı içeriyor ancak **\<main account\> hareketleri** sayfasından veya Alacak hesapları ya da Borç hesapları gibi yanlış bir yardımcı defterden tersine çevriliyor:

    - Bu nedenden de anlaşılacağı gibi Toplu ters işlem özelliği açıkken bile bazı yardımcı defter hareketleri yalnızca belirli sayfalardan tersine çevrilebilir.

- Banka yabancı para birimi yeniden değerleme işlemi:

    - Banka yabancı para birimi yeniden değerleme işlemi tersine çevrilebilir. Ancak ters işlem adımlarını kronolojik sıraya uygun olmayan şekilde tamamlarsanız ters işlem engellenebilir. Örneğin, yeniden değerlemeyi Mart ve Nisan aylarında çalıştırdıysanız Mart yeniden değerlemesi, Nisan yeniden değerlemesi tersine çevrilene kadar tersine çevrilemez.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Tersine çevrilemeyen hareket türleri

Aşağıdaki hareket türleri tersine çevrilemez:

- Elektronik fon transferi (EFT) olarak yapılan satıcı ödemeleri
- Senetler
- Kambiyo senetleri

## <a name="fixed-assets"></a>Sabit kıymetler

Birkaç hareket türü, Sabit kıymetler yardımcı defterini güncelleştirir. Alımlar ve amortisman örnek olarak verilebilir.

Toplu ters işlem özelliği kapatılırsa **Satıcı hareketleri** sayfasından, **Sabit kıymet hareketleri** sayfasından veya hareket türüne göre Varlık kiralamadan hareketler tek tek tersine çevrilebilir.

Toplu ters işlem özelliği açılırsa bir veya daha fazla Sabit kıymet hareketi, hareketlerin deftere nakledildiği günlükteki **Fiş hareketleri** sayfasından da tersine çevrilebilir.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Hareketlerin tersine çevrilememelerinin nedenleri

Hareketler aşağıdaki nedenlerle tersine çevrilemez:

- Mali dönem beklemede veya kalıcı olarak kapalı:

    - Tersine çevirme tarihi açık olmayan bir mali dönemdeyse hareket tersine çevrilemez.
    - Hareket, bir ters işlem tarihinin girişini destekliyorsa ters işlem tarihi açık bir mali döneme değiştirilerek hareket yine de tersine çevrilebilir.

- Genel muhasebe yıl sonu kapanışı işlemi çalıştırıldı:

    - Hareketin muhasebe tarihi, Genel muhasebede kapatılan bir mali yıl içindedir. Mali yıldaki bir dönem hala açık olsa da mali yıl için yıl sonu kapanışı işlemi çalıştırılmışsa hareket tersine çevrilemez. Mali yıl, içindeki dönemlerden farklı bir duruma sahiptir.
    - Yıl sonu kapanışı tersine çevrilebilir ve ardından hareket tersine çevrilebilir. Bu yaklaşım bir seçenek olmayabilir. Mali kapanış işleminin durumuna bağlı olarak kapatılan mali yılın veya sonraki mali yılın açık döneminde bir tersine çevirme hareketini el ile girmek daha kolay olabilir. Yıl sonu kapanışı işleminden geçen mali yılın açık dönemine yeni bir hareket deftere nakledilirse yıl sonu kapanışının yeniden çalıştırılması gerekir.

- Alımlar:

    - Alım, bir satınalma siparişi satıcı faturasıyla gerçekleştiyse ters işlem, bir satıcı alacak dekontu girilerek yapılmalıdır. Ters işlem hareketinin nasıl girileceği hakkında bilgi için bkz. [Satınalma iade emri oluşturma](../../supply-chain/procurement/tasks/create-purchase-return-order.md).
    - Alım, bir proje hareketiyle gerçekleşti.
    - Varlık için amortisman deftere nakledildikten sonra alım tersine çevrilemez. Alımın tersine çevrilebilmesi için önce amortismanın tersine çevrilmesi gerekir.
    - Sabit kıymet için değer modelinin veya amortisman defterinin durumu açık olarak ayarlanmamışsa hareket tersine çevrilemez.

- Elden Çıkarmalar:

    - Elden çıkarma bir serbest metin faturası aracılığıyla yapıldı:

        - Sabit kıymet içeriyorsa serbest metin faturasının düzeltilmesi engellenir. Ancak varlık bir günlük yoluyla elden çıkarılırsa serbest metin faturası, sabit kıymet kaydından tersine çevrilebilir.

    - Sabit kıymet için değer modelinin veya amortisman defterinin durumu açık olarak ayarlanmamışsa hareket tersine çevrilemez.

- Amortisman:

    - Sonraki amortisman da deftere nakledilmişse amortisman tersine **çevrilebilir**. Ancak bu yaklaşım en iyi uygulama olmadığından bir uyarı alırsınız.
    - Sabit kıymet için değer modelinin veya amortisman defterinin durumu açık olarak ayarlanmamışsa hareket tersine çevrilemez.

- Belirli bir varlık ve varlık defteri için hareketler (veya tersine çevrilen hareketler), fişin işlem tarihi veya sonrasındadır.
- Hareket bir varlık hesabı içeriyor ancak **\<main account\> hareketleri** sayfasından veya Alacak hesapları ya da Borç hesapları gibi yanlış bir yardımcı defterden ters çevriliyor:

    - Bu nedenden de anlaşılacağı gibi Toplu ters işlem özelliği açıkken bile bazı yardımcı defter hareketleri yalnızca belirli sayfalardan tersine çevrilebilir.
    - Alım, satınalma siparişi olmayan satıcı faturasında veya satıcı faturası günlüğünde gerçekleştiyse yalnızca Borç hesaplarındaki **Satıcı hareketleri** sayfasından tersine çevrilebilir.
    - Varlık, Varlık kiralamadan alınmışsa Varlık kiralamadaki **Yükümlülük hareketleri** sayfasından tersine çevrilebilir.
