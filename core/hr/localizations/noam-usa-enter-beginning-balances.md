---
title: "Bordro başlangıç bakiyelerini girin"
description: "Bu konu kazanç kodları, kesintiler, kazançlar ve vergiler girmek için gerekli adımları anlatır. Bu bilgiler, İş ortaklarının veriyi bir sistemden yeni bir Bordro uygulama sistemine taşıması veya aktarması için kullanışlıdır."
author: kherr
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 911a51e2498800e7ee7b1562b66c56967eef0505
ms.openlocfilehash: e6213d2e01445b78c6d8f98fc6a55f7c551231b5
ms.contentlocale: tr-tr
ms.lasthandoff: 06/19/2017


---

# <a name="enter-payroll-beginning-balances"></a>Bordro başlangıç bakiyelerini girin

[!include[banner](../../includes/banner.md)]]

Bu konu kazanç kodları, kesintiler, kazançlar ve vergiler girmek için gerekli adımları anlatır. Bu bilgiler, veriyi bir sistemden yeni bir Bordro uygulama sistemine taşıması veya aktaran ortaklar için kullanışlıdır. Bordro bakiyelerini girmeye hazırlanmak için aşağıdaki bilgileri doğrularız:

> * Personel kayıtlarının sisteme girilmiş ve kullanılabilir olması
> * Aşağıdaki verinin personele ayarlanmış ve atanmış olması:

> > * Ödeme döngüleri ve ödeme dönemleri
> > * Kazanç kodları
> > * Vergiler
> > * Kazançlar ve kesintiler

> * Şirket, bordro başlangıç bakiyelerinin ayarlanabileceği bir tarih seçmiş olmalıdır.

> * Bilgi, tüm kazançlardan, kazanç/kesintilerden, kazanç katkılarından, personel vergilerinden ve işveren vergileriyle onların eski sistemden YTD tutarlarından toplanmıştır.

Başlangıç bakiyelerini girmeyi planladığınızda, verinin ne kadar ayrıntılı olması gerektiğini göz önünde bulundurun. Çoğu işletme tek bir birleştirilmiş yılbaşından bugüne tutarını girer Ancak, daha ayrıntılı bilgi gerekiyorsa, bakiyeler üç aylık aralıklarla girilebilir. Gerekli olan ayrıntı seviyesine karar vermek, her bir çalışan için kaç adet el ile ödeme ekstresinin oluşturulması gerektiğini belirler. Tek bir yılbaşından bugüne tutarı için her bir çalışana yalnızca bir el ile ekstre gereklidir. Bunu yapmak için önceki sistemden son ödeme ekstresinin yılbaşından bugüne tutarını, yeni bordro sisteminde girilen tutar olarak kullanın.

Aşağıdaki örnek kazanç kodları, kazançlar, kesintiler ve vergiler de dahil personel bordro başlangıç bakiyelerini nasıl girebileceğinizi gösterir. Bir gerçek dünya örneğinde, her bir kazanç kodu, kazanç kesintisi, kazanç katkısı, personel vergisi ve işveren vergisi için yılbaşından bugüne tutarında girilen tutar satır öğesine sahip olacaksınız. Kodların ve tutarların bu listesini kullanarak, başlangıç bakiyelerini bordo amacıyla getirmek için muhasebe devre dışıyken bir el ile ödeme ve maaş ekstresini oluşturmak için izleyin.  Başlangıç bakiyesi ödeme ekstresini genel muhasebe defterinize nakletmek istemediğiniz için muhasebeyi devre dışı bırakırsınız. Bu eski sistemde yapılmıştır ve Genel muhasebede başlangıç bakiyelerini ayarladığınızda gelecektir.

> [!NOTE] 
> Aşağıdaki adımların aynısını yeniden oluşturmak istiyorsanız Demo verisini kullanabilirsiniz. Demo verileri PartnerSource üzerinden indirilebilir.

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a>A. Bordro başlangıç bakiyelerinde kullanılacak kazanç kodlarının ayarlanması
Bordro başlangıç bakiyeleri girdiğinizde, kullanacağınız kazanç kodlarının "Kazanç ekstresi oranlarının düzenlenmesine izin ver" seçeneği etkin olarak yapılandırılmış olduğundan emin olun. Bu, eski sistemden tutarı el ile girmenize izin verecektir. 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a>B. Bir personelin bir başlangıç bakiyesine sahip olması için kazanç ekstreleri oluşturun
Bu adım, eski sistemin son gün dönemi için, her bir çalışana bir kazanç ekstresini el ile yaratır ve bu da yeni bordro sisteminde kazanç ekstresi satırlarını oluşturur. Kazanç kodu başına bir satır ve YTD tutarını ve saatlerini girin. Örnek adımlar aşağıdaki gibidir:

1. **Tüm kazançlar ekstreleri** sayfasını açın ve **Yeni** üzerine tıklayın.  

Aşağıdakileri girin: 

| Alan      | Değer                 |
|------------|-----------------------|
| Çalışan     | Michael Redmond       |
| Ödeme döngüsü  | sm                    |
| Ödeme dönemi | 16/06/2017- 30/06/2017 |

2. **Kazanç ekstre satırı** sekmesinde aşağıdakini girin:

Satır 1: **Kazanç ekstre satırı** sekmesi

| Alan            | Değer       |
|------------------|-------------|
| Kazançlar kodu    | Düzenli ödeme |
| Miktar         | 1.00        |
| Ücret             | 30.000      |
| Satır ayrıntıları sekmesi |             |
| El ile           | (işaretli)    |

Satır 2: **Kazanç ekstre satırı** sekmesi

| Alan            | Değer    |
|------------------|----------|
| Kazançlar kodu    | Prim    |
| Miktar         | 1,0000   |
| Ücret             | 4250,00  |
| Satır ayrıntıları sekmesi |          |
| El ile           | (işaretli) |

Satır 3: **Kazanç ekstre satırı** sekmesi

| Alan           | Değer      |
|-----------------|------------|
| Kazançlar kodu   | Komisyon |
| Miktar        | 1,0000     |
| Ücret            | !.299,00   |
| Ücret            | 1.299,00   |
| Satır ayrıntı sekmesi |            |
| El ile          | (İşaretli)   |

> [!NOTE]
> **Satır Ayrıntıları** sekmesinde El ile onay kutusu ayarını her bir kazanç ekstre satırını işaretlemek, her bir çalışan için bordro başlangıç bakiyelerinin girilmesini sağlamak için önemlidir.

3. **Eylem** bölmesinde, **Kazanç ekstrelerini serbest bırak** USA-FED-ER-FICA üzerine tıklayın.

4. **Eylem** bölmesinde, **Ödeme ekstresi** üzerine tıklayarak **Ödeme ekstreleri oluştur** sayfasını açın ve aşağıdakileri ayarlayın:

| Alan              | Değer     |
|--------------------|-----------|
| Ödeme tarihi       | 30/06/2017 |
| Ödeme işlemi türü   | El ile    |
| Muhasebeyi devre dışı bırak | (işaretli)  |

> [!NOTE] 
> Bu, yalnızca ödeme yürütme türü el ile olduğunda ve kullanıcının ödeme çalıştırmasında muhasebeyi devre dışı bırakmak istediğinde kullanılabilir.

**Tamam** üzerine tıklayın ve **Bilgi günlüğü**'nü kapatın.

#### <a name="why-disable-accounting-checkbox-needs-to-be-turned-on-when-generating-pay-statements"></a>Ödeme ekstreleri oluştururken Muhasebeyi Devre Dışı Bırak onay kutusu neden açık olmalıdır?
Bu, ödeme ekstresindeki satırların dağıtılmasını ve Genel muhasebeye nakledilmesini engeller. Bu başlangıç bakiyesi ödeme ekstresini, değerleri zaten eski sistemden genel muhasebede olduğu için deftere nakletmek istemezsiniz. Bu bakiye yüklemesi yalnızca raporlama ve sınırlama amaçlarıyla kullanılır.

### <a name="c-create-pay-statements-for-employees"></a>C. Personeller için ödeme ekstreleri oluştur
Başlangıç bakiyelerine sahip ödeme ekstreleri oluşturduktan sonra, ödeme ekstrelerinin bordro verisini doğru şekilde yansıttığını doğrulamanız gerekir. Kazanç ve vergi bilgisini de önceki bordro sistemindeki verilerle eşleşecek şekilde el ile güncelleştirmeniz gerekir. Önceki bordro sisteminden tutarları, geçerli ödeme ekstrelerindeki tutarlarla eşleştiğini doğruladıktan sonra, ödeme ekstrelerini sonlandırmanız gerekir.

1. **Tüm ödeme ekstreleri** sayfasını açın.

2. Michael Redmond için son oluşturulan ödeme ekstresini vurgulayın

3. **Ödeme ekstresi** sayfasını açmak için **Düzenle** üzerine tıklayın.

4. **Kazanç kesintileri** sekmesini açın ve aşağıdakini girin:

| Alan                           | Değer            |
|---------------------------------|------------------|
| Kazanç                         | Kesinti tutarı |
| 401K | Katıl              | 3000,00          |
| Diş | SubSp                  | 495.00           |
| Dep bakım harcaması | Katıl | 2500,00          |
| Görme | SupSp                  | 500.00           |

5. **Kazanç kesintileri** sekmesinde aşağıdakini girin: 

| Alan                           | Değer            |
|---------------------------------|------------------|
| Kazanç                         | Kesinti tutarı |
| 401K | Katıl              | 3000,00          |
| Diş | SubSp                  | 495.00           |
| Dep bakım harcaması | Katıl | 2500,00          |
| Görme | SupSp                  | 500.00           |

6. **Kazanç katkıları** sekmesinde aşağıdakileri girin:

| Alan              | Değer               |
|--------------------|---------------------|
| Kazanç            | Katkı tutarı |
| 401K | Katıl | 3000,00             |
| Diş | SubSp     | 495.00              |
| Görme | SubSp     | 500.00              |

7. **Vergi kesintileri** sekmesinde aşağıdakileri girin:

| Alan           | Değer            |
|-----------------|------------------|
| Vergi kodu.        | Kesinti tutarı |
| USA-FED-ER-FICA | 1600,00          |
| USA-FED-ER-MEDI | 825,75           |

8. **Vergi katkıları** sekmesinde aşağıdakileri girin:

9. **Hesapla** üzerine tıklayın.
> [!IMPORTANT] 
> Çalışan için ödeme ekstresi toplamlarının eski sistemin YTD'si ile eşleştiğini doğrulayın. Tüm ödeme ekstrelerinin toplamında bazı genel doğrulamalar gerçekleştirmek için sonraki adımda sonlandırmayı bekletmek isteyebilirsiniz. Doğrulandıktan sonra, tüm ödeme ekstreleri arasında çalıştırın ve onları sonlandırın.

Aynı işlem gerek duyulursa, yıl içerisindeki tüm önceki çeyrekler için üç aylık aralıklarla yapılabilir. Bu yalnızca müşterinin eski sisteme geri gitmeden veriyi üç alık olarak görmesi gerekiyorsa gereklidir.

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a>Bir Personel için Başlangıç Bakiyelerini girerken bir hata yaptıysanız
Hareketleri geri almak ve yeniden girmek mümkündür. Hareketleri geri almak için tek yapmanız gereken **Tüm ödeme ekstreleri** sayfasında aşağıdaki adımları tamamlamaktır.

1. **Terse çevir** üzerine tıklayın.

2. "Bu ödeme ekstresini geri çevirdiğinizde, bu ödeme ekstresini dengelemek için bir ters ödeme ekstresi oluşturulacaktır" iletisi üzerinde **Evet**'e tıklayın. Hiçbir ödeme ekstresi düzenlenemez. Bu ödeme ekstresini ters çevirmek istiyor musunuz?" görüntülenir. 

Ödeme ekstresini ters çevirdikten sonra, çalışan için yeni bir ödeme ekstresini, bu konuda daha önce belirtilmiş olan "Başlangıç bakiyelerine sahip kazanç ekstreleri ve ödeme ekstreleri oluştur" prosedürünü kullanarak kazanç ekstreleri oluşturabilirsiniz. Yeni bir ödeme ekstresi oluşturmadan önce kazanç ekstresindeki tüm hatalı satırları düzelttiğinizden emin olun ve bu konuda bulunan "Faydalar ve vergiler için başlangıç bakiyelerine sahip ödeme ekstrelerini güncelleştir" prosedürünü tekrar edin.

