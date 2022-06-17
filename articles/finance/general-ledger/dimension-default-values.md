---
title: Mali günlüklerdeki varsayılan mali boyutlar
description: Bu makalede, mali boyut değerlerinin mali günlükler aracılığıyla girilen hareketlerde nasıl ayarlanacağını tanımlayan kurallar açıklanmaktadır. Ayrıca, sabit boyutların kullanıldığı senaryolara ilişkin ayrıntılar da verilmektedir.
author: kweekley
ms.date: 09/04/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransDaily, LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8d0fcf836e22207baae562801fb082d735df0f96
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907948"
---
# <a name="default-financial-dimensions-on-financial-journals"></a>Mali günlüklerdeki varsayılan mali boyutlar

[!include [banner](../includes/banner.md)]

Bu makalede, mali günlükler aracılığıyla (stok yevmiye defterleri veya proje günlükleri aracılığıyla değil) girilen hareketlerde mali boyut değerlerinin nasıl ayarlanacağını tanımlayan kurallar açıklanmaktadır. Ayrıca, sabit boyutların kullanıldığı senaryolara ilişkin ayrıntılar da verilmektedir.

## <a name="symptom"></a>Belirti

Mali boyut değerleri bir mali günlükteki Hesapta veya Mahsup hesabında beklendiği gibi ayarlanmamış. Aşağıdaki senaryolarda iki örnek verilmiştir:

Yevmiye defterine bir fiş girilir. Hesap, satıcı hesabı ve Mahsup hesap, banka hesabıdır. Satıcının mali boyutları Hesaba varsayılan olarak girilir ancak bankanın mali boyutları Mahsup hesaba varsayılan olarak girilmez. Bunun yerine, Hesaptaki boyut değerleri varsayılan olarak Mahsup hesaba girilir.

Müşterinin mali boyut değerleri varsayılan olarak atanmış ve bir gelir ana hesabında Departman mali boyutu için sabit bir boyut değeri atanmıştır. Yevmiye defterine bir fiş girilir.  Hesap müşteri hesabıdır ve Mahsup hesap, özellikle de sabit boyut değerine sahip gelir hesabı türündeki bir genel muhasebe hesabıdır. Sabit boyut, gelir ana hesabı için Mahsup hesapta ayarlanmamıştır. Bunun yerine, müşteriden gelen Hesaptaki Departman boyutu değerine ayarlanmıştır.  Fiş deftere nakledildikten sonra, deftere nakledilen muhasebe girişinde sabit boyut değeri kullanılır ancak fişte, müşterinin gelir hesabındaki departman değeri gösterilmeye devam eder. 

Bir günlükteki fişlerde ayarlanan mali boyut değerleri için hangi kurallar izlenir?

## <a name="resolution"></a>Çözüm

Yevmiye defteri veya satıcı fatura günlüğü gibi mali günlüklerdeki fişlerin satırlarına mali boyut değerlerini varsayılan olarak girmek için aşağıdaki kurallar izlenir. 

1. **Günlük başlığı**

   - Günlük başlığı boyutları, günlük adı boyutlarından varsayılan olarak girilir.

2. **Günlük satırı hesabı**

   - Günlük satırı hesap boyutları, günlük başlığı boyutlarından varsayılan olarak girilir.
   - Boş bir mali boyut varsa bunun değerleri müşteri, satıcı, banka, sabit kıymet, proje veya genel muhasebe boyutlarından varsayılan olarak girilir.

     - Hesap türü **Genel muhasebe** ise genel muhasebe hesabındaki sabit bir boyut, hareket girişi sırasında varsayılan boyut gibi işlem görür.
     - Hesap türü **Müşteri**, **Satıcı**, **Banka**, **Sabit kıymetler** veya **Proje** ise ana hesap henüz belirlenemez. Bu nedenle, hesap için hiçbir zaman varsayılan olarak sabit bir boyut girilmez.

3. **Günlük satırı mahsup hesabı**

 - İlk olarak, günlük satırı Mahsup hesap boyutları, günlük satırı Hesap boyutlarından varsayılan olarak girilir.

 - Boş bir mali boyut varsa sonraki varsayılan giriş Müşteri, Satıcı, Banka, Sabit kıymetler, Proje veya Genel muhasebe boyutlarından alınır.
   1. Mahsup hesap türü **Genel muhasebe** ise Genel muhasebe hesabındaki sabit bir boyut, hareket girişi sırasında varsayılan boyut gibi işlem görür. Hesaptan varsayılan olarak bir boyut değeri zaten girilmişse ana hesabın varsayılan veya sabit boyut değeri mevcut değeri geçersiz kılmaz.
   2. Mahsup hesap türü **Müşteri**, **Satıcı**, **Banka**, **Sabit kıymetler** veya **Proje** ise ana hesap henüz bilinmiyordur; bu nedenle Mahsup hesap için hiçbir zaman varsayılan olarak sabit bir boyut girilmez.

4. **Deftere nakletme**

    1. Deftere nakil sırasında, sabit bir boyut değeri olup olmadığını belirlemek için muhasebe girişinin her satırına ait ana hesap (hem Hesap hem de Mahsup hesap için) değerlendirilir. Sabit bir boyut tanımlanmışsa mevcut veya boş değerler bu sabit boyut değeriyle değiştirilir.

        Sabit boyut değeri, deftere nakledildikten sonra günlük satırlarında **gösterilmez**. Bunun yerine, deftere nakil işleminden sonra fişi görüntülediğinizde muhasebe girişinde gösterilir.

    2. Deftere nakil sırasında eklenebilecek diğer muhasebe hesapları (kuruş yuvarlama ve şirketlerarası borç veya alacak hesapları) dahil olmak üzere başka hiçbir boyut değeri, deftere nakil sırasında varsayılan olarak girilmez. Ek genel muhasebe hesaplarının varsayılan boyut girişleri, Hesaptan veya Mahsup hesaplardan alınır.

Boyut değerlerinin varsayılan olarak girilmesi amacıyla, günlük varsayılan işlemi boş bir boyut değerinin bilerek boş bırakılıp bırakılmadığını veya varsayılan girişin yapılıp yapılmadığını belirleyemez. Bir boyut değeri bilerek boş bırakılmışsa daha önce açıklanan varsayılan değer girme sırası kullanılarak bir değer varsayılan olarak yine de girilebilir. Boyutun boş bir değere sahip olmasını istiyorsanız boş bir boyut yerine kullanılabilmesi için **0** (sıfır) veya **Boş** değerine sahip bir boyut oluşturmanız gerekebilir.

Mali boyut varsayılan değer girme sırası ile ilgili örnekler için aşağıdaki senaryoları inceleyin.

### <a name="scenario-1"></a>Senaryo 1

**Genel muhasebe \> Günlük ayarı \> Günlük adları**'na gidin ve **GenJrn** günlük adını seçin. Daha sonra **Mali boyutlar** hızlı sekmesinde, varsayılan mali boyutlar için aşağıdaki değerleri tanımlayın:

- **BUSINESSUNIT:** 001
- **DEPARTMENT:** 024

[![Günlük adları sayfası](./media/financial-dimension-defaulting-jrnl-names-01.png)](./media/financial-dimension-defaulting-jrnl-names-01.png)

**Genel muhasebe \> Günlük girişleri \> Yevmiye defteri**'ne gidin ve **GenJrn** günlük adını kullanan yeni bir yevmiye defteri oluşturun. Boyutlar, **Mali boyutlar** sekmesinde gösterildiği gibi günlük adından (LedgerJournalName tablosu) günlük başlığına (LedgerJournalTable tablosu) varsayılan olarak girilir.

[![Yevmiye defterleri sayfasındaki Mali boyutlar sekmesi](./media/financial-dimension-defaulting-genrl-jrnl-02.png)](./media/financial-dimension-defaulting-genrl-jrnl-02.png)

**Satırlar**'a gidin. **Hesap türü** alanında **Genel muhasebe**'yi seçin ve ardından **Hesap** alanına **170150** girin. Daha sonra alanın dışına gitmek için **Tab** tuşunu seçin. Boyutlar günlük başlığından varsayılan olarak girilir. Bu nedenle, **Hesap** değeri **170150-001-024** olarak gösterilir.

[![Günlük fişi sayfasındaki yevmiye defterinin günlük satırları](./media/financial-dimension-defaulting-jrnl-vchr-03.png)](./media/financial-dimension-defaulting-jrnl-vchr-03.png)

**Hesap** değerini **170150-001-023** olarak değiştirin. Borç tutarını veya alacak tutarını girin. **Mahsup hesap türü** alanında **Genel muhasebe**'yi seçin ve ardından **Mahsup hesap** alanına **600150** girin. Boyut değerleri hesaptan varsayılan olarak girilir. Bu nedenle, **Mahsup hesap** değeri **600150-001-023** olarak gösterilir.

### <a name="scenario-2"></a>Senaryo 2

Senaryo 1'de günlük adı için tanımladığınız mali boyutları kullanın. Ardından **Alacak hesapları \> Müşteriler \> Tüm müşteriler**'e gidin ve US-001 müşterisi için varsayılan boyut değerlerini tanımlayın. Müşteri ayrıntılarının açılacağı müşteriyi seçin. **Mali boyutlar** sekmesinde **BUSINESSUNIT** boyutu için varsayılan değeri (**001**) koruyun. **COSTCENTER** boyutunu ekleyin ve değer olarak **007** girin.

**GenJrn** günlük adını kullanan yeni bir yevmiye defteri oluşturun. **Mali boyutlar** sekmesinde varsayılan olarak **001** olan **BUSINESSUNIT** değerini **002** olarak değiştirin.

**Satırlar**'a gidin. **Hesap türü** alanında **Müşteri**'yi seçin ve ardından **Hesap** alanına **US-001** girin. Genel muhasebe harici hesap türlerinin mali boyutlarını görüntülemek için **Mali boyutlar \> Hesap**'ı seçin. Mali boyut değerleri için aşağıdaki varsayılan girişler girilir:

- **BUSINESSUNIT:** 002 – Varsayılan giriş, günlük başlığından alınır. Zaten varsayılan bir değer girilmiş olduğundan, **001** değeri US-001 müşterisinden varsayılan olarak girilmez.
- **COSTCENTER:** 007 – Varsayılan giriş, US-001 müşterisinin ayarlarından alınır.
- **DEPARTMENT:** 024 – Varsayılan giriş, günlük başlığından alınır.

Tekrar satıra gelerek **Mahsup hesap türü**'nde **Genel muhasebe**'yi seçin ve ardından **Mahsup hesap** alanına **600150** girin. Aşağıdaki varsayılan mali boyut değerleri satıra girilir:

- **BUSINESSUNIT:** 002 – Varsayılan giriş, hesabın mali boyutlarından alınır. (Başlangıçta günlük başlığından varsayılan olarak girilmişti.)
- **DEPARTMENT:** 024 – Varsayılan giriş, hesabın mali boyutlarından alınır. (Başlangıçta günlük başlığından varsayılan olarak girilmişti.)
- **COSTCENTER:** 007 – Varsayılan giriş, hesabın mali boyutlarından alınır. (Başlangıçta müşteriden varsayılan olarak girilmişti.)

### <a name="scenario-3"></a>Senaryo 3

Senaryo 2 için kullandığınız günlüğe yeni bir satır ekleyin. **Hesap türü** alanında **Genel muhasebe**'yi seçin ve ardından **Hesap** alanına **170150** girin. Varsayılan boyut değerlerini, yalnızca 170150 ana hesabı kalacak şekilde temizleyin. **Mahsup hesap türü** alanında **Müşteri**'yi seçin ve ardından **Mahsup hesap** alanına **US-001** girin. Mali boyut değerleri için aşağıdaki varsayılan girişler girilir:

- **BUSINESSUNIT:** 002 – Hesap boyutu değeri boş olduğundan, varsayılan giriş günlük başlığından alınır. Günlük başlığından varsayılan bir değer zaten alındığından **001** değeri US-001 müşterisinden varsayılan olarak girilmez. **BUSINESSUNIT** değeri bilerek boş bırakılmışsa Mahsup hesaptaki mali boyutu da kaldırmanız gerekir.
- **COSTCENTER:** 007 – Hesap boyutu değeri ve günlük başlığı boyutu değeri boş olduğundan, varsayılan giriş US-001 müşterisinden alınır. **COSTCENTER** değeri bilerek boş bırakılmışsa Mahsup hesaptaki mali boyutu da kaldırmanız gerekir.
- **DEPARTMENT:** 024 – Hesap boyutu değeri boş olduğundan, varsayılan giriş günlük başlığından alınır. **DEPARTMENT** değeri bilerek boş bırakılmışsa Mahsup hesaptaki mali boyutu da kaldırmanız gerekir.

### <a name="scenario-4"></a>Senaryo 4

1 ve 2 numaralı senaryolarda günlük adı ve müşteri için tanımladığınız varsayılan mali boyut değerlerini kullanın. Ardından, 170150 ana hesabındaki **BUSINESSUNIT** boyutu için sabit boyut değerini tanımlayın. **Genel muhasebe \> Hesap planı \> Hesaplar \> Ana hesaplar**'a gidin. **Ana hesap** alanında **170150**'yi seçin ve ardından **Tüzel varlık geçersiz kılmaları** sekmesinde **Ekle**'yi seçin. Tüzel kişilik olarak **USMF**'yi belirleyin, ardından **Ekle**'yi seçin. İlgili kaydı ve ardından **Varsayılan boyutlar**'ı seçin. **BUSINESSUNIT** boyutunu **Sabit değer** olarak değiştirin ve **003** değerini girin.

**GenJrn** günlük adını kullanan yeni bir yevmiye defteri oluşturun. **Mali boyutlar** sekmesinde, varsayılan tüm boyut değerlerini kaldırın.

**Satırlar**'a gidin. **Hesap türü** alanında **Genel muhasebe**'yi seçin ve ardından **Hesap** alanına **170150** girin. Daha sonra alanın dışına gitmek için **Tab** tuşunu seçin. 170150 hesabı için boyut değerleri varsayılan olarak ana hesap ayarlarından girilir. Bu nedenle, **Hesap** değeri **170150-003-** olarak gösterilir.

**Hesap** değerini **170150-004-** olarak değiştirin. **Günlük işlevi sabit bir boyut değerinin değiştirilmesini engellemez.** Borç tutarını veya alacak tutarını girin. **Mahsup hesap türü** alanında **Genel muhasebe**'yi seçin ve ardından **Mahsup hesap** alanına **170250** girin. Mali boyut değeri 004, Hesaptan varsayılan olarak girilir. Ardından belgeyi deftere nakledin. Günlükte **Fiş**'i seçin. Deftere nakil sırasında **BUSINESSUNIT** değerinin **003** sabit boyut değerine geri döndürüldüğünü unutmayın.

Günlükteki fişe geri döndüğünüzde, **BUSINESSUNIT** boyutu sabit boyut değerini **yansıtmaz**. Bu değer her zaman, deftere nakletmeden önce ekranda gösterilen değer olarak kalır. Deftere nakil işlemi, fişe girilen hiçbir değeri değiştirmez. Deftere nakil sırasında yalnızca muhasebe girişi değiştirilir.

## <a name="developer-notes"></a>Geliştirici notları

Geliştiricisiyseniz ve varsayılan değer girme işleminin koduna göz atmak istiyorsanız aşağıdaki yöntemleri inceleyin:

- **LedgerJournalEngine.accountModified()** – Bu yöntem, tüm günlüklerde standart olarak kullanılan (ve bazı günlük türleri tarafından geçersiz kılınan) birincil hesap boyutu varsayılan değer girme işleminin ana giriş noktasıdır.
- **LedgerJournalEngine.offsetAccountModified()** – Bu yöntem, mahsup hesap boyutu varsayılan değer girme işleminin ana giriş noktasıdır.
