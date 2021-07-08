---
title: Döngü sayımı örnek senaryoları
description: Bu konu, Microsoft Dynamics 365 Supply Chain Management'ın döngü sayımı özelliklerini keşfetmek için kullanılan bir senaryo koleksiyonu kullanmaktadır.
author: GalynaFedorova
ms.date: 06/08/2021
ms.topic: article
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage, SalesShipmentDeviation, WHSRFMenuItemCycleCount, WHSWorkLineCycleCount
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 828954402d223c62f52d7a13fcc9efab84630c80
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261805"
---
# <a name="cycle-counting-example-scenarios"></a>Döngü sayımı örnek senaryoları

[!include [banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Supply Chain Management'ın döngü sayımı özelliklerini keşfetmek için kullanılan bir senaryo koleksiyonu kullanmaktadır. Önce mevcut Supply Chain Management ortamınızla ilgili gereksinimleri açıklar. Daha sonra, döngü sayımının nasıl yapılandırılacağını ve tüm döngü sayım aşamalarını açıklar. Bitirdiğinizde, kılavuzlu döngü sayımı, kör döngü sayımı, nokta döngüsü sayımı, döngü sayımı eşikleri ve döngü sayımı planları dahil döngü sayımı hakkında bilgi sahibi olmanız gerekir.

## <a name="prerequisites"></a>Önkoşullar

### <a name="make-demo-data-available"></a>Tanıtım verilerini kullanılabilir hale getirme

Bu konudaki her senaryo, Supply Chain Management için sağlanan standart tanıtım verilerinde bulunan değerler ve kayıtlarla ilgilidir. Senaryolarda ilerlerken burada sağlanan değerleri kullanmak isterseniz tanıtım verisinin yüklü olduğu bir ortamda çalıştığınızdan ve başlamadan önce tüzel kişiliği (şirket) **USMF** olarak ayarladığınızdan emin olun.

### <a name="turn-on-support-for-the-warehouse-management-mobile-app"></a>Warehouse Management mobil uygulaması için desteği açma

Yeni Warehouse Management mobil uygulamasını kullanabilmeniz için, sisteminize yönelik destek eklemeniz gerekir. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Yeni ambar uygulaması için kullanıcı ayarları, simgeler ve adım başlıkları*

### <a name="prepare-demo-data-for-the-scenarios"></a><a name= "prepare-demo-data"></a>Senaryolar için tanıtım verileri hazırlama

Senaryolar için gereken tüm tanıtım verilerinin sisteminizdeki USMF şirketinde kullanılabilir olduğunu onaylamak için aşağıdaki adımları izleyin. Eksik olan kayıt veya değerleri oluşturun.

1. **Ambar yönetimi \> Kurulum \> Çalışan**'a gidin.
1. Liste bölmesinde, **Julia Funderburk**'u seçin.
1. **Kullanıcılar** hızlı sekmesinde, aşağıdaki değerlere sahip satırı seçin. Bu değerleri içeren mevcut satır yoksa, oluşturun.

    - **Kullanıcı kimliği:** *61*
    - **Kullanıcı adı:** *WH61*
    - **Varsayılan ambar:** *61*
    - **Menü adı:** *Ana*

1. **İş** hızlı sekmesinde, önceden ayarlanmamışsa Kullanıcı *61* için aşağıdaki değerleri ayarlayın:

    - **Döngü sayımı gözetmeni:** *Hayır*
    - **Maksimum yüzde sınırı:** *0*
    - **Maksimum miktar sınırı** *0*
    - **Maksimum değer sınırı:** *0*

1. **Ambar yönetimi \> Kurulum \> İş \> İş öğeleri** seçeneğine gidin.
1. İş havuzları, ambar işini iş türüne göre ayrıştırmak için kullanılır (bu durumda, döngü sayım işi). Aşağıdaki ayarlara sahip bir kayıt olduğundan emin olun:

    - **İş havuzu kimliği:** *CycleCount*
    - **Açıklama:** *Döngü Sayımı*

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
1. Liste bölmesinde, *Döngü Sayımı* adlı kaydı seçin. Bu ada sahip bir kayıt yoksa, oluşturun. Kayıt için aşağıdaki değerleri onaylayın veya ayarlayın:

    - **Menü öğesi adı:** *Döngü Sayımı*
    - **Başlık:** *Döngü Sayımı Kılavuzlu*
    - **Mod:** *İş*
    - **Mevcut işi kullan:** *Evet*
    - **Yöneten:** *Sistem tarafından yönetilen* (Bu değer, Supply Chain Management'ın çalışana döngü sayımı iş kodu atayacağı anlamına gelir.)
    - **Stok durumunu görüntüle:** *Evet*

1. Eylem Bölmesinde, **Döngü sayımı**'nı seçin.
1. **Mobil cihaz döngü sayımı** iletişim kutusunda, aşağıdaki değerleri onaylayın veya ayarlayın:

    - **Madde numarasını görüntüle:** *Evet*
    - **Plaka görüntüle:** *Evet*
    - **Deneme sayısı:** *1*

1. İletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Liste bölmesinde, *Döngü Sayımı Kör* adlı kaydı seçin. Bu ada sahip bir kayıt yoksa, oluşturun. Kayıt için aşağıdaki değerleri onaylayın veya ayarlayın:

    - **Menü öğesi adı:** *Döngü Sayımı Kör*
    - **Başlık:** *Döngü Sayımı Kör*
    - **Mod:** *İş*
    - **Mevcut işi kullan:** *Evet*
    - **Yöneten:** *Döngü sayım gruplaması* (Bu değer, çalışanın belirli bir yerleşime, bölgeye veya iş havuzuna özgü döngü sayım işi kimliklerini gruplandırabileceği anlamına gelir.)

1. Eylem Bölmesinde, **Döngü sayımı**'nı seçin.
1. **Mobil cihaz döngü sayımı** iletişim kutusunda, aşağıdaki değerleri onaylayın veya ayarlayın:

    - **Madde numarasını görüntüle:** *Hayır*
    - **Plaka görüntüle:** *Hayır*
    - **Deneme sayısı:** *0*

1. İletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Liste bölmesinde, *Nokta Sayım* adlı kaydı seçin. Bu ada sahip bir kayıt yoksa, oluşturun. Kayıt için aşağıdaki değerleri onaylayın veya ayarlayın:

    - **Menü öğesi adı:** *Nokta Sayımı*
    - **Başlık:** *Nokta Sayımı*
    - **Mod:** *İş*
    - **Varolan çalışmayı kullan:** *Hayır*
    - **İş oluşturma süreci:** *Nokta döngü sayımı* (Bu değer, çalışanın ambar yerleşimindeki maddeleri döngü sayım işi oluşturmaksızın her zaman sayabileceği anlamına gelir. Bir yerleşimde nokta döngü sayımı gerçekleştirmek için çalışan yerleşim kimliğini girer.)

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü**'ne gidin.
1. Liste bölmesinde, *Stok* adlı kaydı seçin. Bu ada sahip bir kayıt yoksa, oluşturun. **Menü yapısı** sütununda aşağıdaki döngü sayım menü öğelerinin göründüğünü onaylayın:

    - Döngü Sayımı
    - Döngü Sayımı Kör
    - Nokta sayımı

1. **Ambar yönetimi \> Kurulum \> Ambar yönetim parametreleri**'ne gidin.
1. **Döngü sayımı** sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Varsayılan döngü sayım ayarlama türü:** *Döngü Sayımı* (Bu alan, döngü sayımı yapıldığında deftere nakledilen günlük türünü belirtir.)
    - **Varsayılan döngü sayım işi sınıf kimliği:** *CCount* (Bu alan, döngü sayımı için kullanılan iş sınıfını belirtir.)
    - **Varsayılan döngü sayımı çalışma önceliği:** *50* (Bu alan, döngü sayım işinin, ambardaki diğer iş türlerine göre sahip olduğu önceliği ayarlar. Diğer iş türleri için girilenden daha düşük bir sayı girerek, döngü sayımı işinin önceliğini artırırsınız.)

1. **Ambar yönetimi \> Kurulum \> Stok \> Ayarlama türleri** öğesine gidin.
1. **Ayarlama türleri** sayfası, ortaya çıkabilecek farklı giriş ve çıkış ayarlamaları için kod oluşturmanıza olanak tanır. Aşağıdaki ayarlara sahip bir kayıt olduğunu onaylayın:

    - **Stok ayarlama türü:** *Döngü Sayımı*
    - **Açıklama:** *Döngü Sayımı*
    - **Ad:** *ICnt*

1. **Ambar yönetimi \> Kurulum \> Ambar kurulumu \> Ambarlar**'a gidin.
1. Liste bölmesinde ambar *61*'i seçin. Bu ada sahip bir kayıt yoksa, oluşturun.
1. **Ambar** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Ambar yönetimi işlemini kullan:** *Evet* (Bu değer ambar yönetimi işlemleri için ambarı etkinleştirir.)
    - **Döngü sayımı sırasında plakaya izin ver:** *Evet* (Bu değer, çalışanların döngü sayımı sırasında plakaları taşımasına olanak sağlar.)

## <a name="scenario-1-guided-cycle-counting"></a>Senaryo 1: Kılavuzlu döngü sayımı

Kılavuzlu döngü sayımının gerçekleşmesi için önce bazı işler oluşturmanız gerekir. Bu iş, işte atanan kişiye ambar boyunca (yerleşimden yerleşime) iş içinde ayarlanan sayımları tamamlaması için yol gösterecektir.

### <a name="create-cycle-counting-work-for-scenario-1"></a>Senaryo 1 için döngü sayım işi oluşturma

Ambar *61*'deki *01A02R2S2B* (BULK-06) madde yerleşimi için döngü sayımı oluşturmak üzere bu adımları izleyin.

1. **Ambar Yönetimi \> Kurulum \> Yerleşime göre döngü sayımı işi**'ne gidin.
1. **Yerleşime göre döngü sayımı oluştur** iletişim kutusunda, **İş havuzu kimliği** alanını *CycleCount* olarak ayarlayın.
1. **Eklenecek kayıtlar** hızlı sekmesinde **Filtrele**'yi seçin.
1. Sorgu düzenleyici iletişim kutusunda **Aralık** sekmesinde şu adımları izleyin:

    - **Alan** alanının *Ambar* olarak ayarlandığı satır için **Ölçüt** alanını *61* olarak ayarlayın.
    - **Alan** alanının *Yerleşim* olarak ayarlandığı satır için **Ölçüt** alanını *01A02R2S2B* olarak ayarlayın.

1. Sorgu düzenleyicisi iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. **Yerleşime göre döngü sayımı işi oluştur** iletişim kutusunu kapatmak için **Tamam**'ı seçin.

    İş oluşturma işlemi tamamlandığında, Eylem merkezinde bir ileti görüntülenir.

1. **Ambar yönetimi \> İş \> İş ayrıntıları**'na gidin.
1. **CycleCount** değerine sahip kayıtları bulmak için *İş havuzu kimliği* sütununda filtre ayarlayarak yeni oluşturulan işi bulun.

### <a name="do-cycle-counting-work-for-scenario-1"></a>Senaryo 1 için döngü sayımı işi yapma

Döngü sayımı işi oluşturduktan sonra, döngü sayım işini bir ambar yerleşimindeki maddeleri sayıp sonuçları bir mobil cihaz kullanarak Supply Chain Management'a girerek gerçekleştirirsiniz. Warehouse Management mobil uygulamasında döngü sayımı işini yapmak için bu adımları izleyin.

1. Bu konunun önceki bölümlerinde yer alan [Senaryolar için tanıtım verileri hazırlama](#prepare-demo-data) bölümünde ayarladığınız iş kullanıcısı olarak Warehouse Management mobil uygulamasında oturum açın. Bu konudaki örnek için, kullanıcı *Julia Funderburk* adına sahiptir ve ambar *61* için ayarlanmıştır. (USMF demo verileri, kullanıcı kimliği olarak *61* ve parola olarak *1* girerek bu iş kullanıcısı olarak oturum açmanıza olanak tanıyacaktır.)
1. Ana menüde **Stok**'u seçin.
1. **Stok** menüsünde, **Döngü Sayımı Kılavuzlu** öğesini seçin.
1. **Miktar** alanını seçin, sayısal tuş takımını kullanarak *9* girin ve ardından **Tamam**'ı (onay işareti düğmesi) seçin.
1. Sistem bu madde, yerleşim ve plaka için 10 parçalık sayı girmenizi bekliyordu. Bu nedenle, tekrar sayım yapmanız istendi. **Miktar** alanını seçin, sayısal tuş takımını kullanarak tekrar *9* girin ve ardından **Tamam**'ı (onay işareti düğmesi) seçin. İkinci denemede, sayımızın kabul edilecektir.

    > [!NOTE]
    > Sistem beklenen eldeki miktar ile girdiğiniz miktar arasında bir fark algıladığında, **Deneme sayısı** alanı **Döngü Sayımı Kılavuzlu** mobil cihaz menü öğesi için *1* olarak ayarlandığından, ikinci kez saymanızı istedi. Mobil cihaz menü öğesi için **Madde numarası görüntüle** ve **Plaka görüntüle** seçeneği *Evet* olarak ayarlanmış olduğundan, belirli bir madde numarası ve plaka numarasına yönlendirildiniz.

1. **Tamam**'ı (onay işareti düğmesi) seçin.

### <a name="review-the-cycle-counting-differences-for-scenario-1"></a>Senaryo 1 için döngü sayım farklarını gözden geçirme

Döngü sayım farklılıklarını gözden geçirmek için bu adımları izleyin.

1. Supply Chain Management'a dönün.
1. **Ambar yönetimi \> İş \> İş ayrıntıları**'na gidin.
1. Daha önce bakmış olduğunuz döngü sayımı işini bulun ve seçin. (Örneğin, *CycleCount* değerine sahip kayıtları bulmak için **İş havuzu kimliği** sütununda filtre ayarlayın.) Bu iş için **İş durumu** alanının artık *Gözeen geçirme bekleniyor* olarak ayarlandığına dikkat edin.

    > [!NOTE]
    > Sayım işini yapmak için kullandığınız iş kullanıcı hesabı için, **Döngü sayımı yöneticisi** seçeneği *Hayır* olarak, **Maksimum yüzde sınırı**, **Maksimum miktar sınırı** ve **Maksimum değer sınırı** alanlarının tümü *0* (sıfır) olarak ayarlanır. Bu nedenle, bu kullanıcının raporladığı tüm sayım farklarının el ile onaylanması gerekir ve ilgili işin **İş durumu** alanı *Gözden geçirme bekliyor* olarak ayarlanır. Sayılan değer, sapma sınırları içindeyse (**İş kullanıcıları** sayfasında **Maksimum yüzde sınırı** veya **Maksimum miktar sınırı** alanlarında belirtildiği gibi) veya **Döngü sayımı yöneticisi** seçeneği kullanıcı için *Evet* olarak ayarlanmışsa, iş otomatik olarak kapatılır.

1. Eylem Bölmesindeki **İş** sekmesinde, **Döngü Sayımı**'nı seçin.
1. Eylem Bölmesinde, **Sayımı kabul et**'i seçin.

    Fark, standart sayım günlüğü kullanılarak deftere nakledilir ve yeni bir iş emri oluşturulur.

1. **Döngü sayım hareketleri** sayfasında, Eylem bölmesinde, onaylanan fark için oluşturulan işi bulmak için **Türetilmiş iş**'i seçin.

## <a name="scenario-2-blind-cycle-counting"></a>Senaryo 2: Kör döngü sayımı

Bu senaryo, sisteminizde senaryo 1'in tamamlanmış olmasını gerektirir.

### <a name="create-cycle-counting-work-for-scenario-2"></a>Senaryo 2 için döngü sayım işi oluşturma

Kör döngü sayımının gerçekleşmesi için önce bazı işler oluşturmanız gerekir. Ambar *61*'deki *01A02R2S2B* (BULK-06) madde yerleşimi için döngü sayımı oluşturmak üzere bu adımları izleyin.

1. **Ambar Yönetimi \> Kurulum \> Maddeye göre döngü sayımı işi**'ne gidin.
1. **Maddeye göre döngü sayımı oluştur** iletişim kutusunda, **İş havuzu kimliği** alanını *CycleCount* olarak ayarlayın.
1. **Eklenecek kayıtlar** hızlı sekmesinde **Filtrele**'yi seçin.
1. Sorgu düzenleyicisi iletişim kutusunda **Aralık** sekmesinde, aşağıdaki ayarlara sahip üç satır ekleyin:

    - Satır 1:

        - **Tablo:** *Maddeler*
        - **Alan:** *Madde numarası*
        - **Ölçüt:** *L0101*

    - Satır 2:

        - **Tablo:** *Stok boyutları*
        - **Alan:** *Ambar*
        - **Ölçüt:** *61*

    - Satır 3:

        - **Tablo:** *Stok boyutları*
        - **Alan:** *Yerleşim*
        - **Ölçüt:** *01A02R2S2B*

1. Sorgu düzenleyicisi iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. **Maddeye göre döngü sayımı işi oluştur** iletişim kutusunu kapatmak için **Tamam**'ı seçin.

    İş oluşturma işlemi tamamlandığında, bir bilgi iletisi alırsınız.

### <a name="do-cycle-counting-work-for-scenario-2"></a>Senaryo 2 için döngü sayımı işi yapma

Döngü sayımı işini oluşturduktan sonra, Warehouse Management mobil uygulamasında döngü sayımı işini yapmak için bu adımları izleyin.

1. Bu konunun önceki bölümlerinde yer alan [Senaryolar için tanıtım verileri hazırlama](#prepare-demo-data) bölümünde ayarladığınız iş kullanıcısı olarak Warehouse Management mobil uygulamasında oturum açın. Bu konudaki örnek için, kullanıcı *Julia Funderburk* adına sahiptir ve ambar *61* için ayarlanmıştır. (USMF demo verileri, kullanıcı kimliği olarak *61* ve parola olarak *1* girerek bu iş kullanıcısı olarak oturum açmanıza olanak tanıyacaktır.)
1. Ana menüde **Stok**'u seçin.
1. **Stok** menüsünde, **Döngü Sayımı Kör** öğesini seçin.
1. **Bölge kodu** alanını seçin *BULK06* girin ve sonra **Tamam**'ı (onay işareti düğmesi) seçin.
1. **Madde** alanını seçin *L0101* girin ve sonra **Tamam**'ı (onay işareti düğmesi) seçin.
1. **Plaka** alanını seçin *LP\_BULK\_06\_01* girin ve sonra **Tamam**'ı (onay işareti düğmesi) seçin.
1. **Miktar** alanını seçin *10* girin ve sonra **Tamam**'ı (onay işareti düğmesi) seçin.

    > [!NOTE]
    > Sistem beklenen eldeki miktar ile taradığınız miktar arasında bir fark algılasa bile, **Deneme sayısı** alanı **Döngü Sayımı Kör** mobil cihaz menü öğesi için *0* (sıfır) olarak ayarlandığından, ikinci kez saymanızı istemedi. Mobil cihaz menü öğesi için **Madde numarası görüntüle** ve **Plaka görüntüle** seçeneği *Hayır* olarak ayarlanmış olduğundan, madde numarasını ve plaka numarasını taramanız istendi.

1. **Tamam**'ı (onay işareti düğmesi) seçin.

### <a name="review-the-cycle-counting-differences-for-scenario-2"></a>Senaryo 2 için döngü sayım farklarını gözden geçirme

Döngü sayım farklılıklarını gözden geçirmek için bu adımları izleyin.

1. Supply Chain Management'a dönün.
1. **Ambar yönetimi \> Genel \> İş \> İnceleme bekleyen döngü sayımı işi**'ne gidin.
1. Eylem Bölmesindeki **İş** sekmesinde, **Döngü Sayımı**'nı seçin.
1. Eylem Bölmesinde, **Sayımı reddet**'i seçin.

    Sayım farkı reddedildiği için iş kapatılır.

## <a name="scenario-3-spot-cycle-counting"></a>Senaryo 3: Nokta döngü sayımı

Eldeki stok kaydı *01A02R2S2B* yerleşiminde *L0101* maddesi için eldeki stok bulunduğunu belirtir. Ambar çalışanı *01A02R2S1B* yerleşimindedir. Bu yerleşim boş olması gerekmesine karşın doludur. Bu nedenle, ambar çalışanı hemen bu yerleşim için nokta sayımı yapar.

### <a name="do-cycle-counting-work-for-scenario-3"></a>Senaryo 3 için döngü sayımı işi yapma

Warehouse Management mobil uygulamasında döngü sayımı işini yapmak için bu adımları izleyin.

1. Bu konunun önceki bölümlerinde yer alan [Senaryolar için tanıtım verileri hazırlama](#prepare-demo-data) bölümünde ayarladığınız iş kullanıcısı olarak Warehouse Management mobil uygulamasında oturum açın. Bu konudaki örnek için, kullanıcı *Julia Funderburk* adına sahiptir ve ambar *61* için ayarlanmıştır. (USMF demo verileri, kullanıcı kimliği olarak *61* ve parola olarak *1* girerek bu iş kullanıcısı olarak oturum açmanıza olanak tanıyacaktır.)
1. Ana menüde **Stok**'u seçin.
1. **Stok** menüsünde, **Nokta sayımı** öğesini seçin.
1. **Yerleşim** alanını seçin *01A02R2S1B* girin ve sonra **Tamam**'ı (onay işareti düğmesi) seçin.

    Sistem, Supply Chain Management'ta yerleşimin boş olduğunu algılar.

1. **LP veya Öğe Ekle**'yi seçin.
1. **Madde** alanını seçin *L0101* girin ve sonra **Tamam**'ı (onay işareti düğmesi) seçin.
1. **Plaka** alanını seçin *LP\_BULK\_06\_01* girin ve sonra **Tamam**'ı (onay işareti düğmesi) seçin.
1. **Miktar** alanını seçin *9* girin ve sonra **Tamam**'ı (onay işareti düğmesi) seçin.

    Sistem belirtilen plakanın Supply Chain Management'ta başka bir yerleşimde zaten kullanılabilir olduğunu algıladığı için, bu plaka geçerli yerleşime taşınacaktır. Bu nedenle, sistem hareketi onaylamanızı ister.

1. **Tamam**'ı (onay işareti düğmesi) seçin.

### <a name="review-the-cycle-counting-differences-for-scenario-3"></a>Senaryo 3 için döngü sayım farklarını gözden geçirme

Sayım sonuçlarını gözden geçirmek için bu adımları izleyin.

1. Supply Chain Management'a dönün.
1. **Ambar yönetimi \> Genel \> İş ayrıntıları**'na gidin.
1. Kılavuzun en üstündeki **Kapalı olanı göster** onay kutusunu seçin.
1. **İş emri türü** sütunu için filtreyi *Stok hareketi* olarak ayarlayın.

    Sistem bu sayımı stok hareketi olarak otomatik olarak algıladı. **Döngü sayımı sırasında plaka hareketlerine izin ver** seçeneği, *Ambarlar* sayfasında ambar *61* için **Evet** olarak ayarlandığından, bu harekete izin verilir.

## <a name="scenario-4-define-cycle-count-thresholds"></a>Senaryo 4: Döngü sayımı eşiklerini tanımlama

Döngü sayım işi oluşturmanın bir yolu eşikler kullanmaktır. Bir döngü sayımı eşiği stok maddelerinin miktar veya yüzde sınırını belirtir. Döngü sayımı işi, eşiğe ulaşıldığında otomatik olarak oluşturulur.

Örneğin, döngü sayımı eşiği 40 olan bir yerleşimde 60 öğe vardır. Bir satış siparişi hareketi sırasında, 25 öğe konumdan alınır ve bir hazırlama konumuna koyulur. 35 olan yeni madde sayısı, eşik miktarından az olduğundan döngü sayım işi bu konum için otomatik olarak oluşturulur.

Döngü sayımı eşiklerini ayarlamak için aşağıdaki adımları takip edin:

1. **Ambar yönetimi \> Kurulum \> Döngü sayımı \> Döngü sayımı eşikleri** öğesine gidin.
1. Eylem Bölmesinde, bir eşik oluşturmak için **Yeni**'yi seçin ve bunun için aşağıdaki değerleri ayarlayın:

    - **Döngü sayımı eşiği kodu:** *L0101*
    - **Açıklama:** *Eşik L0101*
    - **Eşik miktarı:** *2*
    - **Birim:** *ea*
    - **Yüzdeye dayalı kapasite eşiği:** *0,00*
    - **Döngü sayımı eşik türü:** *Miktar*
    - **Döngü sayımını hemen işle:** *Evet*
    - **Döngü sayımı arasındaki günler:** *1*
    - **İş havuzu kimliği:** *CycleCount*

1. Eylem Bölmesinde, **Madde seç**'i seçin.
1. Sorgu düzenleyicisi iletişim kutusunda, **Aralık** sekmesinde, **Alan** alanının *Madde sayısı* olarak ayarlandığı satırı bulun. Bu satır için **Ölçüt** alanını *L0101* olarak ayarlayın.
1. Sorgu düzenleyicisi iletişim kutusunu kapatmak için **Tamam**'ı seçin.

    Şimdi madde *L0101* için döngü sayımı eşiğini tanımladınız.

Eldeki miktar 2'den küçükse ve yerleşime ait son döngü sayımının tarihi bugün değilse, herhangi bir yerleşimdeki madde *L0101* için döngü sayımı oluşturulur.

## <a name="scenario-5-define-cycle-count-plans"></a>Senaryo 5: Döngü sayımı planlarını tanımlama

Döngü sayımı planları döngü sayım işi oluşturmayı otomatikleştirmenize olanak sağlar. Her döngü sayım planını belirli madde ve yerleşim sorgularıyla ayarlayabilirsiniz. Toplu iş çalıştırıldığında, madde ve yerleşim ölçütüyle eşleşen tüm yerleşimler için döngü sayımı işi oluşturulur (plan için belirtilen maksimum sayım sayısına kadar). Döngü sayım işi oluşturulduğunda, sayım iş satırı sayım yapılması gereken yerleşim hakkında bilgi içerir. Bu yerleşimle ilişkilendirilmiş eldeki stok bloke değildir. Bu nedenle, açık sayım işi olsa bile, rezervasyon ve giden işlem için kullanılabilir.

Döngü sayımı planı ayarlamak için aşağıdaki adımları takip edin:

1. **Ambar yönetimi \> Kurulum \> Döngü sayımı \> Döngü sayımı planları** öğesine gidin.
1. Eylem Bölmesinde, ızgaraya satır eklemek için **Yeni**'yi seçin ve ardından aşağıdaki değerleri ayarlayın:

    - **Döngü sayım planı kodu:** *BULK06*
    - **Açıklama:** *BULK06 için yerleşim sayımı*
    - **İş havuzu kimliği:** *CycleCount*
    - **Maksimum döngü sayımı sayısı:** *10*
    - **Döngü sayımı arasındaki günler:** *10*
    - **Boş yerleşimler:** *Boş olanı hariç tut*
    - **İş şablonu:** Bu alanı boş bırakın.

1. Eylem Bölmesinde, **Yerleşimleri seç**'i seçin.
1. Standart sorgu düzenleyicisi iletişim kutusu görüntülenir. **Aralık** sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Tablo:** *Yerleşimler*
    - **Alan:** *Bölge Kodu*
    - **Ölçüt:** *BULK06*

1. Sorgu düzenleyicisi iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Eylem Bölmesinde, **Döngü sayımı planını işle**'yi seçin.
1. **Döngü sayımı planları** iletişim kutusunda **Arka planda çalıştır** hızlı sekmesinde, **Toplu işleme** seçeneğini *Evet* olarak ayarlayın.
1. **Yineleme**'yi seçin.
1. **Yinelemeyi tanımla** iletişim kutusunda, toplu işi hemen başlayıp her dakikada bir çalışacak şekilde ayarlayın; bitiş tarihi olmaz.
1. **Yinelemeyi tanımla** iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. **Döngü sayımı planları** iletişim kutusunu kapatmak için **Tamam**'ı seçin.

    Bir ileti, işin toplu iş kuyruğuna eklendiğini bildirir.

1. **Ambar yönetimi \> Ortak \> Döngü sayımı planlama**'ya gidin. Plan hemen başlar ve sayım işi oluşturur. Sayım işi tamamlanmadığından, **Durum** alanı *İşleniyor* olarak ayarlanır. Bir dakikada sonra, **Toplam döngü sayısı** sütunundaki değer *1* olarak değişir.

    > [!NOTE]
    > Son döngü sayımından sonra geçen gün sayısı, döngü sayım planı için **Döngü sayımı arasındaki günler** alanı için ayarladığınız değerden azsa, döngü sayımı işi oluşturulmaz. Örneğin, **Döngü sayımı arasındaki günler** alanı *5* olarak ayarlanmışsa, döngü sayımı işi her beş günde bir oluşturulur. Ancak, döngü sayım işi üçüncü günde işleniyorsa, bir sonraki döngü sayım işi son döngü sayımı işlendikten beş gün sonra, sekizinci gün içinde oluşturulur.

1. Eylem Bölmesinde oluşturulan sayım işini görüntülemek için **İş**'i seçin.
