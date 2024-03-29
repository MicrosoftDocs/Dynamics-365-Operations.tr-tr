---
title: Performans sorunlarını gidermek için ER biçimlerinin yürütülmesini izleme
description: Bu makale, performans sorunlarını gidermek amacıyla Elektronik raporlama (ER) uygulamasındaki performans izleme özelliğinin nasıl kullanılacağı hakkında bilgi sağlar.
author: kfend
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: 9f088228b140a42ee097c9e810166550ab0fae81
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289959"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a>Performans sorunlarını gidermek için ER biçimlerinin yürütülmesini izle

[!include[banner](../includes/banner.md)]

Elektronik raporlama (ER) konfigürasyonlarının elektronik belgeler oluşturmak amacıyla tasarlanması işleminin bir parçası olarak, uygulamadan veri elde etmek ve oluşturulan çıktıya girmek için kullanılan yöntemi tanımlayın. ER performans izleme özelliği, ER biçim yürütmesi ve performans sorunlarını gidermek için onları kullanma ile ilgili zamanı ve maliyeti önemli ölçüde azaltmaya yardımcı olur. Bu kılavuz, yürütülen ER biçimleri için performans izlemelerinin nasıl alınacağı ve performansın artırılmasına yardımcı olmak amacıyla bu izlemelerin nasıl kullanılacağı hakkında yönergeler sağlar.

## <a name="prerequisites"></a>Önkoşullar

Bu kılavuzdaki örnekleri tamamlamak için şu erişimlere sahip olmanız gerekir:

- Aşağıdaki rollerden birine erişim:

    - Elektronik raporlama geliştirici
    - Elektronik raporlama işlev danışmanı
    - Sistem yöneticisi

- Aşağıdaki rollerden biri için, uygulamanınkiyle aynı kiracı için sağlanan Regulatory Configuration Services (RCS) örneğine erişim:

    - Elektronik raporlama geliştirici
    - Elektronik raporlama işlev danışmanı
    - Sistem yöneticisi

Ayrıca, aşağıdaki dosyaları da indirip yerel olarak depolamalısınız.

| Dosya                                  | İçerik                               |
|---------------------------------------|---------------------------------------|
| Performans izleme modeli sürüm 1     | [Örnek ER verisi modeli yapılandırması](https://download.microsoft.com/download/0/a/a/0aa84e48-8040-4c46-b542-e3bf15c9b2ad/Performancetracemodelversion.1.xml)    |
| Performans izleme meta veri sürüm 1  | [Örnek ER meta verisi yapılandırması](https://download.microsoft.com/download/a/9/3/a937e8c4-1f8a-43e4-83ee-7d599cf7d983/Performancetracemetadataversion.1.xml)      |
| Performans izleme eşleştirme sürümü 1.1 | [Örnek ER model eşleme yapılandırması](https://download.microsoft.com/download/7/7/3/77379bdc-7b22-4cfc-9b64-a9147599f931/Performancetracemappingversion1.1.xml) |
| Performans izleme biçimi sürümü 1.1  | [Örnek ER biçim yapılandırması](https://download.microsoft.com/download/8/6/8/868ba581-5a06-459e-b173-fb00f038b37f/Performancetraceformatversion1.1.xml)       |

### <a name="configure-er-parameters"></a>ER parametrelerini yapılandırma

Uygulamada oluşturulan her bir ER performans izleme, yürütme günlükleri kaydının bir eki olarak depolanır. Belge yönetimi (DM) çerçevesi, bu ekleri yönetmek için kullanılır. Performans izlemelerini iliştirmek için kullanılması gereken DM belge türünü belirtmek için ER parametrelerini önceden yapılandırmalısınız. **Elektronik raporlama** çalışma alanında, **Elektronik raporlama parametreleri** bağlantısını seçin. Sonra, **Elektronik raporlama parametreleri** sayfasında, **Ekler** sekmesinde, **Diğerleri** alanında, performans izlemeleri için kullanılacak DM belge türünü seçin.

![Elektronik raporlama parametreleri sayfası.](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

**Diğer** arama alanında kullanılabilmesi için bir DM belgesi türünün aşağıdaki şekilde **Belge türleri** sayfasında yapılandırılması gerekir (**Kuruluş yönetimi \> Belge yönetimi \> Belge türleri**):

- **Sınıf:** Dosya iliştir
- **Grup:** Dosya

![Belge türleri sayfası.](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> DM ekleri şirkete özgü olduğundan, seçilen belge türü, geçerli örneğin tüm şirketlerinde kullanılabilir olmalıdır.

### <a name="configure-rcs-parameters"></a>RCS parametrelerini yapılandırma

Oluşturulan ER performans izlemeleri, ER biçim Tasarımcısı ve ER eşleme Tasarımcısı kullanılarak analiz için RCS'ye aktarılır. ER performans izleri ER biçimiyle ilgili yürütme günlükleri kaydının ekleri olarak depolandığından, RCS parametrelerini önceden yapılandırmalısınız, böylece performans izlemelerini iliştirmek için kullanılacak DM belge türü belirtilebilir. Şirketiniz için sağlanmış olan RCS örneğinde, **Elektronik raporlama** çalışma alanında, **Elektronik raporlama parametreleri**'ni seçin. Sonra, **Elektronik raporlama parametreleri** sayfasında, **Ekler** sekmesinde, **Diğerleri** alanında, performans izlemeleri için kullanılacak DM belge türünü seçin.

![RCS içindeki Elektronik raporlama parametreleri sayfası.](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

**Diğer** arama alanında kullanılabilmesi için bir DM belgesi türünün aşağıdaki şekilde **Belge türleri** sayfasında yapılandırılması gerekir (**Kuruluş yönetimi \> Belge yönetimi \> Belge türleri**):

- **Sınıf:** Dosya iliştir
- **Grup:** Dosya

## <a name="design-an-er-solution"></a>Bir ER çözümü tasarla

Satıcı hareketleri sunan yeni bir rapor oluşturmak üzere yeni bir ER çözümü tasarladığınızı varsayın. Şu anda, seçilen satıcı için hareketleri **Satıcı hareketleri** sayfasında bulabilirsiniz (**Borç hesapları \> Satıcılar \> Tüm satıcılar**'a gidin, bir satıcı seçin ve Eylem Panosu üzerinde, **Satıcı** sekmesinde, **Hareketler** grubunda, **Hareketler**'i seçin). Ancak, tüm satıcı hareketinin elektronik bir belgede XML biçiminde aynı anda olmasını istersiniz. Bu çözüm, gerekli veri modelini, meta verileri, model eşlemeyi ve biçim bileşenlerini içeren birkaç ER yapılandırmasından oluşur.

1. Şirketiniz için sağlanan RCS örneğine oturum açın.
2. Bu kılavuzda, **Litware, Inc.** örnek şirket için yapılandırmalar oluşturacak ve değiştireceksiniz. Bu nedenle, bu konfigürasyon sağlayıcısının RCS'ye eklenmiş olduğundan ve etkin olarak seçildiğinden emin olun. Yönergeler için bkz. [Yapılandırma sağlayıcıları oluşturmak ve bunları etkin olarak işaretlemek yordamına](tasks/er-configuration-provider-mark-it-active-2016-11.md) bakın.
3. **Elektronik raporlama** çalışma alanında **Raporlama yapılandırmaları** kutucuğunu seçin.
4. **Yapılandırmalar** sayfasında, önkoşul olarak karşıdan yüklediğiniz ER yapılandırmalarını aşağıdaki sırada içe aktarın: veri modeli, meta veriler, model eşleme, biçim. Her bir yapılandırma için şu adımları izleyin:

    1. Eylem Panosunda, **Exchange \> XML dosyasından yükle**'yi seçin.
    2. Gerekli ER yapılandırması için XML biçiminde uygun dosyayı seçmek için **Gözat**'ı seçin.
    3. **Tamam**'ı seçin.

    ![RCS'deki Yapılandırmalar sayfası.](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a>Çalışmayı izlemek için ER çözümünü çalıştırın

ER çözümünün ilk sürümünü tasarlamayı bitirdiğinizi varsayalım. Şimdi bunu örneğinizde test etmek ve yürütme performansını analiz etmek istiyorsunuz.

### <a name="import-an-er-configuration-from-rcs-into-finance-and-operations"></a><a id='import-configuration'></a>ER yapılandırmasını RCS'ten Finans ve operasyon'a içeri aktarma

1. Uygulama örneğinizde oturum açın.
2. Bu kılavuzda, yapılandırmaları RCS örneğinizden (ER bileşenlerinizi tasarladığınız yerden) örneğinize (test edeceğiniz ve son olarak kullanacağınız) içe aktarırsınız. Bu nedenle, gerekli tüm yapıların hazırlandığından emin olmalısınız. Talimatlar için bkz. [Düzenleyici Yapılandırma Hizmeti'nden (RCS) Elektronik raporlama (ER) yapılandırmalarını içe aktarma](rcs-download-configurations.md) yordamı.
3. Yapılandırmaları RCS'den uygulamada içe aktarmak için aşağıdaki adımları izleyin:

    1. **Elektronik raporlama** çalışma alanında, **Litware, Inc.** yapılandırma sağlayıcısının döşemesi üzerinde **Depolar**'ı seçin.
    2. **Yapılandırma deposu** sayfasında, **RCS** türünün deposunu seçin ve sonra **Aç**'ı seçin.
    3. **Yapılandırmalar** hızlı sekmesinde, **Performans izleme biçimi** yapılandırmasını seçin.
    4. **Sürümler** hızlı sekmesinde seçilen yapılandırmanın sürüm **1.1**'ini ve sonra **İçe aktar**'ı seçin.

    ![Yapılandırma deposu sayfası.](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

Veri modeli ve model eşleme yapılandırmalarının ilgili sürümleri, içe aktarılan ER biçim konfigürasyonu için önkoşul olarak otomatik içe aktarılır.

### <a name="turn-on-the-er-performance-trace"></a>ER performans izlemesini aç

1. **Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırmalar** seçeneğine git.
2. **Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.
3. **Kullanıcı parametreleri** iletişim kutusunda, **Yürütme izleme** bölümünde şu adımları izleyin:

    1. **Yürütme izleme biçimi** alanda, yürütme ayrıntılarının ER biçimi ve eşleme öğelerinde depolanması gereken oluşturulmuş performans izlemesinin biçimini belirtin:

        - **Hata ayıklama izleme biçimi**: Kısa yürütme süresine sahip bir ER biçimini etkileşimli olarak çalıştırmayı planlıyorsanız bu değeri seçin. Böylece, ER biçimi yürütme ile ilgili ayrıntılar topluluğu başlatılır. Bu değer seçildiğinde, performans izlemesi aşağıdaki eylemlerde harcanan süre hakkında bilgi toplar:

            - Her bir veri kaynağını veri almak için çağırılan model eşlemesinde çalıştırma
            - Oluşturulan çıktıya veri girmek için her biçim öğesini işlemek

            **Hata ayıklama izleme biçimi** değerini seçerseniz, izleme içeriğini ER İşlem tasarımcısında analiz edebilirsiniz. Burada, izlemede bahsedilen ER biçimini veya eşleme öğelerini görüntüleyebilirsiniz.

        - **Toplama izleme biçimi**: Toplu iş modunda uzun yürütme süresine sahip bir ER biçimini çalıştırmayı planlıyorsanız bu değeri seçin. Böylece, ER biçimi yürütme ile ilgili toplama ayrıntıları topluluğu başlatılır. Bu değer seçildiğinde, performans izlemesi aşağıdaki eylemlerde harcanan süre hakkında bilgi toplar:

            - Her bir veri kaynağını veri almak için çağırılan model eşlemesinde çalıştırma
            - Her bir veri kaynağını veri almak için çağırılan biçim eşlemesinde çalıştırma
            - Oluşturulan çıktıya veri girmek için her biçim öğesini işlemek

            **Toplu izleme biçimi** değeri, Microsoft Dynamics 365 Finance 10.0.20 ve sonraki sürümlerde kullanılabilir.

            ER biçim tasarımcısı ve ER model eşleme tasarımcısında, tek bir bileşen için toplam yürütme süresini görüntüleyebilirsiniz. Ek olarak izleme, yürütme sayısı ve tek bir yürütmenin minimum ve maksimum süresi gibi yürütme ayrıntılarını içerir.

            > [!NOTE]
            > Bu izleme, izlenen bileşenler yoluna göre toplanır. Bu nedenle, tek bir üst bileşen birkaç adlandırılmamış alt bileşen içerdiğinde veya birden fazla alt bileşen aynı ada sahip olduğunda istatistikler yanlış olabilir.

    2. ER model eşleme ve ER biçimde bileşenlerinin yürütülmesine dair belirli ayrıntıları toplamak için aşağıdaki seçenekleri **Evet** olarak ayarlayın:

        - **Sorgu istatistiklerini topla** – Bu seçenek etkinleştirildiğinde, performans izlemesi aşağıdaki bilgileri toplar:

            - Veri kaynakları tarafından yapılan veritabanı çağrılarının sayısı
            - Veritabanına yapılan yinelenen çağrıların sayısı
            - Veritabanı çağrılarını yapmak için kullanılan SQL deyimlerinin ayrıntıları

        - **Önbelleğe alma erişimini izleme** – Bu seçenek açıldığında, performans izlemesi ER modeli eşlemesinin önbellek kullanımıyla ilgili bilgilerini toplar.
        - **Veri erişimini izle** – Bu seçenek etkinleştirildiğinde, performans izlemesi kayıt listesi türünün yürütülmüş veri kaynakları için veritabanına yapılan çağrı sayısıyla ilgili bilgi toplar.
        - **Liste numaralandırmasını izle** – Bu seçenek etkinleştirildiğinde, performans izlemesi kayıt listesi türünün veri kaynakları için talep edilen kayıtların sayısı hakkında bilgi toplar.

    > [!NOTE]
    > **Kullanıcı parametreleri** iletişim kutusundaki parametreler kullanıcıya ve geçerli şirkete özgüdür.

    ![Kullanıcı parametreleri iletişim kutusu.](./media/GER-PerfTrace-GER-UserParameters.png)

### <a name="run-the-er-format"></a><a id='run-format'></a>ER biçimini çalıştır

1. **DEMF** şirketini seçin.
2. **Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırmalar** seçeneğine git.
3. **Yapılandırmalar** sayfasında, yapılandırma ağacında , **Performans izleme biçimi** öğesini seçin.
4. Eylem Bölmesinde, **Çalıştır**'ı seçin.

Oluşturulan dosyanın altı satıcıda bulunan 265 hareketleri temsil ettiğine dikkat edin.

## <a name="review-the-execution-trace"></a>Yürütme izlemesini gözden geçirin

### <a name="export-the-generated-trace-from-the-application"></a><a id='export-trace'></a>Oluşturulan izlemeyi uygulamadan dışa aktarın

Performans izlemeleri, kaynak ER biçiminden alınır ve harici bir ZIP dosyasına serileştirilebilir.

1. **Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırma hata ayıklama günlükleri**'ne gidin.
2. **Elektronik raporlama yürütme günlükleri** sayfasında, sol tarafta, **Yapılandırma adı** alanında, **Performans izleme biçimi**'ni seçerek, **Performans izleme biçimi** yapılandırması yürütülmesi tarafından oluşturulan günlük kayıtlarını bulabilirsiniz.
3. Sayfanın sağ üst köşesindeki **Ekler** düğmesini (ataş simgesi) seçin veya **Ctrl+Shift+A**'ya basın.

    ![Elektronik raporlama yürütme günlükleri sayfasındaki Ekler düğmesi.](./media/GER-PerfTrace-GER-DebugLog.png)

4. **Elektronik raporlama yürütme günlükleri için ekler** sayfasında, Eylem Panosunda, **Aç**'ı seçerek performans izlemeyi bir zip dosyası olarak elde edin ve yerel olarak depolayın.

    ![Elektronik raporlama yürütme günlükleri için ekler.](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> Oluşturulan izleme, yalnızca **GUID** biçimindeki benzersiz bir rapor tanımlayıcısı aracılığıyla kaynak ER raporuna referans sağlar. Biçimin sürüm numaralandırması dikkate alınmıyor.

Çalıştırılan ve ER model eşleme için oluşturulan performans izleme arasındaki ilişkinin, kullanılan kök tanımlayıcısını ve ortak veri modelini temel aldığına dikkat edin. Biçim ve model eşleşmesinin sürüm numaralandırması dikkate alınmıyor. **Model eşleme için varsayılan** bayrağı ayarı da dikkate alınmıyor.

### <a name="import-the-generated-trace-into-rcs"></a><a id='import-trace'></a>Oluşturulan izlemeyi RCS'ye içe aktarın

1. RCS içinde, **Elektronik raporlama** çalışma alanında **Raporlama yapılandırmaları** kutucuğunu seçin.
2. **Yapılandırmalar** sayfasında, yapılandırma ağacında, **Performans izleme modeli** öğesini genişletin ve **Performans izleme biçimi** öğesini seçin.
3. Eylem Bölmesinde, **Tasarımcı**'yı seçin.
4. **Biçim tasarımcısı** sayfasında, Eylem Panosu üzerinde, **Performans izleme**'yi seçin.
5. **Performans izleme sonucu ayarları** iletişim kutusunda, **Performans izleme içe aktar**'ı seçin.
6. **Gözat**'ı seçerek, daha önce içe aktardığınız zip dosyasını seçin.
7. **Tamam**'ı seçin.

    ![RCS içindeki performans izleme sonuç ayarları iletişim kutusu.](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a>RCS- Biçim yürütme içindeki analiz için performans izlemesini kullan

1. RCS içinde, **Biçim tasarımcısı** sayfasında, **Genişlet/daralt**'ı seçerek tüm biçim öğelerinin içeriğini genişletin.

    Geçerli biçimin bazı öğeleri için ek bilgiler gösterdiğine dikkat edin:

    - Biçim öğesini kullanarak oluşturulan çıktıya veri girişi için harcanan gerçek süre
    - Aynı zaman, tüm çıktının oluşturulması için harcanan toplam sürenin yüzdesi olarak ifade edilen saat

    ![RCS'deki biçim tasarımcısı sayfası.](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. **Biçim tasarımcısı** sayfasını kapatın.

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><a id='use-trace'></a>RCS- Model eşleme içindeki analiz için performans izlemesini kullan

1. RCS içinde, **Yapılandırmalar** sayfasında, yapılandırma ağacında , **Performans izleme eşleme** öğesini seçin.
2. Eylem Bölmesinde, **Tasarımcı**'yı seçin.
3. **Tasarımcı**’yı seçin.
4. **Model eşleme tasarımcısı** sayfasında, Eylem Panosu üzerinde, **Performans izleme**'yi seçin.
5. Daha önce içe aktardığınız izlemeyi seçin.
6. **Tamam**'ı seçin.

Geçerli model eşleştirmesinin bazı veri kaynağı öğeleri için yeni bilgiler kullanılabilir hale geldiğini dikkate alın:

- Veri kaynağı kullanılarak veri almada harcanan gerçek süre
- Aynı zaman, tüm model eşleşmesinin yürütülmesi için harcanan toplam sürenin yüzdesi olarak ifade edilen saat

ER'ın, geçerli model eşlemesinin, VendTable/\<Relations/VendTrans.VendTable\_AccountNum veri kaynağı yürütüldüğünde veritabanı isteklerini yinelediğine dair sizi bilgilendirdiğine dikkat edin. Bu yineleme, satıcı hareketleri listesinin her tekrarlanmış satıcı kaydı için iki kez çağrılıyor olmasından kaynaklanır:

- Yapılandırılmış bağlamalar temelinde, veri modelindeki her hareketin ayrıntılarını girmek için bir çağrı yapılır.
- Bir arama, veri modelindeki satıcı başına hesaplanan hareket sayısını girmek için gerçekleştirilir.

![RCS'de model eşleme tasarımcısı sayfasındaki yinelenen veritabanı istekleri hakkında ileti.](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

**\[Q:530\]** değeri, VendTrans tablosunun bu tablodan bir kaydı VendTable/\<Relations/VendTrans.VendTable\_AccountNum veri kaynağına iade etmek için 530 kez adlandırdığını gösterir. **\[530\]** değeri, VendTable/\<Relations/VendTrans.VendTable\_AccountNum veri kaynağının bu veri kaynağından bir kayıt döndürmek ve bunu veri modeli içindeki ayrıntıları girmeleri için 530 defa çağrıldığını gösterir.

265 hareketin ayrıntılarını elde etmek için yapılan çağrı sayısını azaltmak ve model eşlemesinin performansını artırmaya yardımcı olmak için VendTable/\<Relations/VendTrans.VendTable\_AccountNum veri kaynağı için önbelleğe almayı kullanmanızı öneririz.

LedgerTransTypeList veri kaynağına yapılan çağrıların sayısını azaltmak için de yararlı olabilir. Bu veri kaynağı, **LedgerTransType** numaralandırmasının her bir değerini etiketiyle ilişkilendirmek için kullanılır. Bu veri kaynağını kullanarak, her bir satıcı hareketi için uygun bir etiket bulabilir ve bunu veri modeline girebilirsiniz. Bu veri kaynağına yapılan çağrı sayısı (9.027), 265 hareket için oldukça yüksektir.

![RCS'de, veri kaynağına uygulanacak 9.027 çağrıyı gösteren model eşleme tasarımcısı sayfası.](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>Yürütme izlemesinin bilgilerine dayalı olarak model eşlemeyi geliştirin

### <a name="modify-the-logic-of-the-model-mapping"></a>Model eşlemenin mantığını değiştirin

1. Veritabanına yinelenen aramaların engellenmesine yardımcı olmak amacıyla önbelleğe alma için şu adımları izleyin:

    1. RCS'de, **Model eşleme tasarımcısı** sayfasında, **Veri kaynakları** bölmesinde, **VendTable** öğesini seçin.
    2. **Önbellek**'i seçin.
    3. **VendTable** öğesini genişletin, VendTable veri kaynağı için bir-çok ilişkisi listesini genişletin (**\<İlişkiler** öğesi) ve **VendTrans.VendTable\_AccountNum** maddesini seçin.
    4. **Önbellek**'i seçin.

    ![Yinelenen çağrıların engellenmesine yardımcı olmak için kurulumu önbelleğe alma.](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. LedgerTransTypeList veri kaynağını VendTable veri kaynağının kapsamına getirmek için aşağıdaki adımları izleyin:

    1. **Veri kaynağı türleri** bölmesinde, **İşlevler** öğesini genişletin ve **Hesaplanan alan** öğesini seçin.
    2. **Veri kaynakları** bölmesinde, **VendTable** öğesini seçin.
    3. **Ekle**'yi seçin.
    4. **Ad** alanına, **\$TransType** girin.
    5. **Formül düzenle**’yi seçin.
    6. **Formül** alanında, **LedgerTransTypeList** girin.
    7. **Kaydet**'i seçin.
    8. **Formül düzenleyici** sayfasını kapatın.
    9. **Tamam**'a tıklayın.

3. **\$TransType** alanının önbelleğe alınması için aşağıdaki adımları izleyin:

    1. **LedgerTransTypeList** öğesini seçin.
    2. **Önbellek**'i seçin.
    3. **VendTable.\$TransType** öğesini seçin.
    4. **Önbellek**'i seçin.

    ![$TransType alanı için önbelleğe alma kurulumu.](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. **\$TransTypeRecord** alanını, önbelleğe alınmış **\$TransType** alanını kullanmaya başlayacak şekilde değiştirmek için şu adımları izleyin:

    1. **Veri kaynakları** bölmesinde **VendTable** öğesini genişletin, **\<İlişkiler** öğesini genişletin, **VendTrans.VendTable\_AccountNum** öğesini genişletin ve **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** öğesini seçin.
    2. **Düzenle** öğesini seçin.
    3. **Formül düzenle**’yi seçin.
    4. **Formül** alanında, aşağıdaki ifadeyi bulun:

        FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))

    5. **Formül** alanında, aşağıdaki ifadeyi girin:

        FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).

    6. **Kaydet**'i seçin.
    7. **Formül düzenleyici** sayfasını kapatın.
    8. **Tamam**'ı seçin.

5. **Kaydet**'i seçin.
6. **Model eşleme tasarımcısı** sayfasını kapatın
7. **Model eşlemeleri** sayfasını kapatın

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>ER model eşlemesinin değiştirilmiş sürümünü tamamlayın

1. RCS'de, **Yapılandırmalar** sayfasında, **Sürümler** hızlı sekmesinde, **Performans izleme eşleme** yapılandırmasının sürüm **1.2**'sini seçin.
2. **Durumu değiştir**'i seçin.
3. **Tamamlandı**'yı seçin.

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-the-application"></a>Değiştirilen ER model eşleme yapılandırmasını RCS'den uygulamada içe aktarma

**Performans izleme eşleştirme** yapılandırması 1.2 sürümünü içeri aktarmak için bu makalenin önceki kısımlarında yer alan [ER yapılandırmasını RCS'ten Finans ve operasyon'a içeri aktarma](#import-configuration) bölümündeki adımları yineleyin.

## <a name="run-the-modified-er-solution-to-trace-execution"></a>Çalışmayı izlemek için değiştirilmiş ER çözümünü çalıştırın

### <a name="run-the-er-format"></a>ER biçimini çalıştır

Yeni bir performans izleme oluşturmak için bu makalenin önceki kısımlarında yer alan [ER biçimini çalıştırma](#run-format) bölümündeki adımları tekrar edin.

## <a name="work-with-the-execution-trace"></a>Yürütme izlemesiyle çalışma

### <a name="export-the-generated-trace-from-the-application"></a>Oluşturulan izlemeyi uygulamadan dışa aktarma

Yeni bir performans izlemesini yerel olarak kaydetmek için bu makalede daha önce ele alınan [Oluşturulan izlemeyi uygulamadan dışarı aktarma](#export-trace) bölümündeki adımları tekrar edin.

### <a name="import-the-generated-trace-into-rcs"></a>Oluşturulan izlemeyi RCS'ye içe aktarın

Bu makalede daha önce ele alından [Oluşturulan izlemeyi RCS'ye içe aktarma](#import-trace) bölümündeki adımları, yeni performans izlemesini RCS'ye aktarmak için tekrar edin.

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a>RCS- Model eşleme içindeki analiz için performans izlemesini kullan

Bu makalenin önceki kısımlarında yer alan [RCS - Model eşleme'deki analiz için performans izlemesini kullanma](#use-trace) bölümündeki adımları en son performans izlemeyi analiz etmek için tekrar edin.

Model eşleştirmesinde yaptığınız ayarlamaların veritabanındaki yinelenen sorguları elediğine dikkat edin. Bu model eşleme için veritabanı tablolarına ve veri kaynaklarına yapılan çağrı sayısı da azaltılmıştır. Bu nedenle, tüm ER çözümü performansı iyileştirilmiştir.

![RCS'de VendTable veri kaynağı için Model eşleme tasarımcısı sayfasında izleme bilgisi.](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

İzleme bilgisinde, VendTable veri kaynağı için değer **\[12\]**, bu veri kaynağının 12 kere çağrıldığını ifade eder. **\[Q:6\]**, VendTable tablosuna çağrıların altısının veritabanı çağrılarına dönüştürüldüğünü gösterir. **\[C:6\]** değeri, veritabanından alınan kayıtların önbelleğe alınmış olduğunu ve başka altı çağrının önbellek kullanılarak işlendiğini ifade eder.

LedgerTransTypeList veri kaynağına yapılan çağrı sayısının 9.027'den 240'a kadar azaltıldığına dikkat edin.

![RCS'de LedgerTransTypeList veri kaynağı için Model eşleme tasarımcısı sayfasında izleme bilgisi.](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-the-application"></a>Uygulamadaki yürütme izlemesini inceleyin

RCS'ye ek olarak, bazı sürümler bir ER çerçeve tasarımcısı deneyimi için yetenekler sağlayabilir. Bu sürümlerde, açılabilir bir **Tasarım modunu etkinleştir** seçeneği vardır. Bu seçeneği, **Elektronik raporlama** çalışma alanından açabileceğiniz **Elektronik raporlama parametreleri** sayfasının **Genel** sekmesinde bulabilirsiniz.

![Elektronik raporlama parametreleri sayfasında Tasarım modunu etkinleştir seçeneği.](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

Bu sürümlerden birini kullanıyorsanız, oluşturulan performans izlemelerinin ayrıntılarını uygulamada doğrudan analiz edebilirsiniz. Bunları uygulamadan dışa aktarmanız ve RCS'de içe aktarmanız gerekmez.

## <a name="review-the-execution-trace-by-using-external-tools"></a>Yürütme izlemesini harici araçlar kullanarak gözden geçirme

### <a name="configure-user-parameters"></a>Kullanıcı parametrelerini yapılandırma

1. **Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırmalar** seçeneğine git.
2. **Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.
3. **Kullanıcı parametreleri** iletişim kutusunda, **Yürütme izleme** bölümünde, **Yürütme izleme biçimi** alanında **PerfView XML** öğesini seçin.

### <a name="run-the-er-format"></a>ER biçimini çalıştır

Yeni bir performans izleme oluşturmak için bu makalenin önceki kısımlarında yer alan [ER biçimini çalıştırma](#run-format) bölümündeki adımları tekrar edin.

Web tarayıcısının karşıdan yüklenmek üzere bir zip dosyası sunduğuna dikkat edin. Bu dosya, PerfView biçiminde performans izlemesini içerir. Daha sonra, PerfView performans analizi aracını, ER biçimi yürütmesinin ayrıntılarını analiz etmek için kullanabilirsiniz.

![PerfView biçiminde performans izleme bilgileri.](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a>Veritabanı sorgularını içeren bir yürütme izlemesini gözden geçirmek için harici araçlar kullanın

ER çerçevesinde yapılan geliştirmeler sayesinde, PerfView formatında oluşturulan performans izleme, şimdi ER biçimi yürütme hakkında daha ayrıntılı bilgi sunmaktadır. Microsoft Dynamics 365 Finance 10.0.4 sürümünde (2019 Temmuz) yürütülen bu izleme, SQL sorgularının ayrıntılarını uygulama veritabanına da ekleyebilir.

### <a name="configure-user-parameters"></a>Kullanıcı parametrelerini yapılandırma

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.
3. **Kullanıcı parametreleri** iletişim kutusunda, **Yürütme izleme** bölümünde aşağıdaki parametreleri ayarlayın:

    - **Yürütme izleme biçimi** alanında, **PerfView XML** öğesini seçin.
    - **Sorgu istatistiklerini** topla seçeneğini **Evet** olarak ayarlayın.
    - **Sorguyu izle** seçeneğini **Evet** olarak ayarlayın.

    ![Yürütme izleme bölümü, Kullanıcı parametreleri iletişim kutusu.](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a>ER biçimini çalıştır

Yeni bir performans izleme oluşturmak için bu makalenin önceki kısımlarında yer alan [ER biçimini çalıştırma](#run-format) bölümündeki adımları tekrar edin.

Web tarayıcısının karşıdan yüklenmek üzere bir zip dosyası sunduğuna dikkat edin. Bu dosya, PerfView biçiminde performans izlemesini içerir. Daha sonra, PerfView performans analizi aracını, ER biçimi yürütmesinin ayrıntılarını analiz etmek için kullanabilirsiniz. Bu izleme şimdi, ER biçiminin yürütülmesi sırasında SQL veritabanı erişimi ayrıntılarını içermektedir.

![PerfView'da yürütülen ER formatı için izleme bilgileri.](./media/GER-PerfTrace2-PerfViewTrace2.PNG)

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik Raporlamaya genel bakış](general-electronic-reporting.md)
- [Parametreli HESAPLANAN ALAN veri kaynakları ekleyerek ER çözümleri performansını iyileştirme](er-calculated-field-ds-performance.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

