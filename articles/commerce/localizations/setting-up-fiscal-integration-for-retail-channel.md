---
title: Commerce kanalları için mali tümleştirmeyi ayarlama
description: Bu makale, mali tümleştirme işlevini Commerce kanalları için ayarlama hakkında yönergeler sağlar.
author: EvgenyPopovMBS
ms.date: 04/28/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 695f3c1e704f2712f392d0d7179da63f47731f46
ms.sourcegitcommit: 6616b969afd6beb11a79d8e740560bf00016ea7f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/17/2022
ms.locfileid: "9027070"
---
# <a name="set-up-the-fiscal-integration-for-commerce-channels"></a>Commerce kanalları için mali tümleştirmeyi ayarlama

[!include [banner](../includes/banner.md)]

Bu makale, mali tümleştirme işlevini Commerce kanalları için ayarlama hakkında yönergeler sağlar. Mali tümleştirme hakkında daha fazla bilgi için bkz. [Commerce kanalları için mali tümleştirme genel bakışı](fiscal-integration-for-retail-channel.md).

## <a name="enable-features-in-commerce-headquarters"></a>Commerce genel merkezinde özellikleri etkinleştirme

Commerce kanallarla ilgili mali tümleştirme işlevleriyle ilişkili özellikleri etkinleştirmek için aşağıdaki adımları izleyin.

1. Commerce genel merkezinde, **Sistem yönetimi \> Çalışma alanları \> Özellik yönetimi**'ne gidin.
1. Aşağıdaki özellikleri bulup etkinleştirin:

    - **POS kasalarının direkt mali tümleştirmesi** – Bu özellik, satış noktasında çalıştırılacak mali bağlayıcılar oluşturma yeteneğini ekleyerek mali tümleştirme çerçevesini uzatır (POS). Bu tür bağlayıcı, bir HTTP uygulama programlama arabirimi (API) sağlayan ve depoda adanmış bir fiziksel makine gerektirmeyen bir mali aygıt veya hizmetle iletişim kurar. Örneğin, bu işlev, paylaşılan donanım istasyonu gerekmeksizin mobil cihazlar için mali tümleştirmeyi etkinleştirir.
    - **Mali tümleştirme teknik profili geçersiz kılmaları** – Bu özellik, mali tümleştirmenin konfigürasyonunun genişletilmesini sağlar ve bir POS kaydının ayarlar sayfasındaki bağlantı parametrelerine denetleme yeteneğini ekler. Bu özellik etkinleştirildiğinde, teknik profilin parametrelerini geçersiz kılabilirsiniz.
    - **POS kayıtlarının mali kayıt durumu** – Bu özellik etkinleştirildiğinde, belirli bir POS kayıtları için mali kayıt işlemini devre dışı bırakabilirsiniz. Bir POS kaydı için mali kayıt devre dışı bırakılmışsa, bu kasada satış hareketleri tamamlanamaz.
    - **Mali tümleştirme yerel depolama ortamı yedekleme** – Bu özellik mali tümleştirme çerçevesinin hata işleme yeteneklerini uzatır. Ayrıca, bir aygıt etkinleştirilirken yerel depolama birimindeki verilerin geri yüklenmesi için, veri kaybı durumunda mali kayıt verilerinin otomatik yedeklemesini de sağlar.

## <a name="set-up-commerce-parameters"></a>Commerce parametrelerini ayarlama

Commerce parametrelerini ayarlamak için aşağıdaki adımları izleyin.

1. **Commerce paylaşılan parametreler** sayfasında, **Genel** sekmesinde, **Mali tümleştirmeyi etkinleştir** seçeneğini **Evet** olarak ayarlayın.
1. **Numara serileri** sekmesinde, aşağıdaki referanslar için numara serilerini tanımlayın:

    - Mali teknik profil numarası
    - Mali bağlayıcı grubu numarası
    - Kayıt işlemi numarası

1. **Commerce parametreleri** sayfasında, mali işlevsel profil numarası için numara serilerini tanımlayın.

> [!NOTE]
> Numara serileri isteğe bağlıdır. Tüm mali tümleştirme varlıkları için numaralar, numara serilerinden veya el ile tanımlanabilir.

## <a name="set-up-a-fiscal-registration-process"></a>Mali kayıt işlemi ayarlamak

Mali tümleştirme Kurulumu işlemi aşağıdaki görevleri içerir:

- Mali aygıt veya mali yazıcı gibi mali kayıt amacıyla kullanılan hizmetleri gösteren mali yapılandırma.
- Mali aygıt veya hizmetler tarafından mali bağlayıcı kaydedilecek mali belgelerin belge sağlayıcılarını yapılandırın.
- Mali kayıt işlemi tanımlayan mali kayıt adımları ve mali bağlayıcı ve her adım için kullanılan sağlayıcıları mali belge sırasını yapılandır.
- Mali kayıt işlemini satış noktası işlev profillerine atayın.
- Donanım profilleri için bağlayıcı teknik profilleri atayın.
- POS donanım veya işlev profilleri için bağlayıcı teknik profilleri atayın.

### <a name="upload-configurations-of-fiscal-document-providers"></a>Mali belge sağlayıcılarının yapılandırmalarını yükleme

Bir mali belge sağlayıcısı, işlemlerini temsil eden mali belgeleri ve POS içerisinde, mali cihaz veya servis ile etkileşimde kullanılan kayıtları oluşturmaktan sorumludur. Örneğin, bir mali belge sağlayıcı XML biçiminde bir mali giriş gösterimi oluşturabilir.

Mali belge sağlayıcılarının yapılandırmalarını yüklemek için bu adımları izleyin.

1. Commerce Headquarters'da **Mali belge sağlayıcıları** sayfasına gidin (**Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali belge sağlayıcıları**).
1. Kullanmayı planladığınız her aygıt veya hizmet için bir XML yapılandırması yükleyin.

> [!TIP]
> **Görünüm**'ü seçerek, geçerli mali belge sağlayıcı ile ilişkili tüm işlev profillerini görebilirsiniz.

> [!NOTE]
> Veri eşleme mali belge sağlayıcının parçası olarak kabul edilir. Aynı bağlayıcı için farklı veri eşlemeleri (mesela özel durum düzenlemeleri), farklı mali belge sağlayıcıları oluşturmanız gerekir.

### <a name="upload-configurations-of-fiscal-connectors"></a>Mali bağlayıcıların yapılandırmalarını yükleme

Bir mali cihaz veya hizmeti ile iletişim için mali bağlayıcı sorumludur. Örneğin, bir mali bağlayıcı, bir mali belge sağlayıcısının XML biçiminde oluşturudğu bir mali girişi, bir mali yazıcıya gönderebilir. Mali tümleştirme bileşenleri hakkında daha fazla bilgi için bkz. [Mali cihazlar ve hizmetler için mali kayıt işlemi ve mali tümleştirme örnekleri](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

Mali bağlayıcıların yapılandırmalarını yüklemek için bu adımları izleyin.

1. Commerce Headquarters'da **Mali bağlayıcılar** sayfasına gidin (**Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali bağlayıcılar**).
1. Mali tümleştirme amacıyla, kullanmayı planladığınız her aygıt veya hizmet için bir XML yapılandırması yükleyin.

> [!TIP]
> **Görünüm**'ü seçerek, geçerli mali bağlayıcı ile ilişkili tüm işlevleri ve teknik profilleri görebilirsiniz.

Mali bağlayıcıların ve mali belge sağlayıcıların yapılandırma örnekleri için bkz. [Commerce SDK'deki mali tümleştirme örnekleri](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-commerce-sdk).

### <a name="create-connector-functional-profiles"></a>Yeni bağlayıcı işlevsel profilleri oluşturma

Bağlayıcı işlevsel profili oluşturmak için bu adımları izleyin.

1. Commerce Headquarters'da **Bağlayıcı işlevsel profilleri** sayfasına gidin (**Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Bağlayıcı işlevsel profilleri**).
1. Bir mali bağlayıcıyla ilgili her mali bağlayıcı ve mali belge sağlayıcısı kombinasyonu için bu adımları izleyerek her şirket için bir bağlayıcı işlev profili oluşturmalısınız.

    1. Bir bağlayıcı adı seçin.
    1. Bir belge sağlayıcı seçin.

#### <a name="change-data-mapping-parameters-in-a-connector-functional-profile"></a>Bir bağlayıcı işlev profilinde veri eşleme parametrelerini değiştirme

Bir bağlayıcı işlev profilinde veri eşleme parametrelerini değiştirebilirsiniz. Aşağıdaki tabloda, bir bağlayıcı işlev profilinde veri eşleme parametrelerinin bazı örnekleri verilmiştir.

| Parametre | Biçim | Örnek |
|-----------|--------|---------|
| KDV oranı ayarları | değer: VATrate | 1 : 2000, 2 : 1800 |
| KDV kodları eşlemesi | VATcode : değer | vat20: 1, vat18: 2 |
| Ödeme türleri eşlemesi | TenderType : değer | Nakit: 1, Kart: 2 |

**Bağlayıcı işlevsel profilleri** sayfasında mali belge sağlayıcı yapılandırmasındaki varsayılan parametreleri geri yüklemek için **Güncelleştir**'i seçin.

> [!NOTE]
> Bağlayıcı işlev profilleri şirkete özeldir. Bir mali bağlayıcı ve mali belge sağlayıcısının kombinasyonunu farklı şirketler için kullanmayı planlıyorsanız her şirket için bir bağlayıcı işlev profili oluşturmalısınız.

### <a name="create-connector-technical-profiles"></a>Yeni bağlayıcı teknik profilleri oluşturma

Bağlayıcı teknik profili oluşturmak için bu adımları izleyin.

1. Commerce Headquarters'da **Bağlayıcı teknik profilleri** sayfasına gidin (**Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Bağlayıcı teknik profilleri**).
1. Bu adımları tamamlayarak her mali bağlayıcı için bir bağlayıcı teknik profili oluşturun:

    1. Bir bağlayıcı adı seçin.
    1. Bir bağlayıcı türü seçin:

        - Bir donanım istasyonuna bağlı olan veya yerel ağda bulunan aygıtlar veya hizmetler için **Yerel**'i seçin.
        - Harici hizmetler için **Harici**'yi seçin.
        - Commerce Runtime ( CRT) içindeki dahili bağlayıcılar için yönelik **Dahili**'yi seçin. 

    1. Bir bağlayıcı konumu seçin:

        - Bağlayıcı donanım istasyonındaysa **Donanım İstasyonu**'nu seçin.
        - Bağlayıcı, POS masasında üzerinde yer alıyorsa **Kasa**'yı seçin.

Bir bağlayıcı teknik profilindeki **Cihaz** ve **Ayarlar** sekmesindeki parametreler değiştirilebilir. Mali bağlayıcı yapılandırmasındaki varsayılan parametreleri geri yüklemek için **Güncelleştir**'i seçin. XML yapılandırmasının yeni sürümü yüklenirken, halihazırda kullanımda olan geçerli mali bağlayıcı veya mali belge sağlayıcıyı belirten bir ileti alırsınız. Bu yordam daha önce bir bağlayıcı işlev profili ve bağlayıcı teknik profillerinde el ile yapılmış olan değişiklikleri geçersiz kılmaz. Yeni bir yapılandırmadan varsayılan parametreler kümesini uygulamak için **Bağlayıcı işlev profilleri** sayfası veya **Bağlayıcı teknik profilleri** sayfasında **Güncelleştir**'i seçin.

Tek bir POS kasası veya mağazası için belirli parametreler ayarlamanız gerekiyorsa, aşağıdaki adımları izleyin.

1. **Geçesiz kıl** menü öğesini seçin.
1. **Geçersiz kıl** sayfasında, yeni bir kayıt oluşturun.
1. Bir mağaza veya POS kasası seçin. Tek bir POS kasası veya tüm POS kasaları için belirli bir mağazadaki seçili teknik profilin parametrelerini geçersiz kılabilirsiniz.
1. **Aygıt** sekmesinde, seçili POS kaydı veya mağazaya ait parametreleri girin.

### <a name="create-fiscal-connector-groups"></a>Mali bağlayıcı grupları oluşturma

Bir mali bağlayıcı grubu, aynı işlevleri gerçekleştiren ve mali kayıt işleminin aynı adımında kullanılan mali bağlayıcıların fonksiyonel profillerini birleştirir. Örneğin, çok sayıda mali yazıcı modeli bir mağazasında kullanılabiliyorsa, bu mali yazıcılar için mali bağlayıcılar bir mali bağlayıcı grubunda birleştirilebilir.

Mali bağlayıcı grubu oluşturmak için aşağıdaki adımları izleyin.

1. **Mali bağlayıcı grubu** sayfasına (**Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali bağlayıcı gruplar**) gidin.
1. Yeni bir mali bağlayıcı grubu oluşturun.
1. Konnektör grubuna işlevsel profiller ekleyin. **İşlev profilleri** sekmesinde, **Ekle**'yi seçin ve bir profil numarası seçin. Mali bağlayıcı grubundaki her bir mali bağlayıcı yalnızca bir işlevsel profile sahip olabilir.
1. Fonksiyonel profilinin kullanımını durdurmak için **Devre dışı bırak** seçeneğini **Evet** olarak seçin. Bu değişiklik yalnızca geçerli bağlayıcı grubu etkiler. Bağlayıcı başka gruplarda aynı işlev profili kullanmak için devam edebilirsiniz.

### <a name="create-a-fiscal-registration-process"></a>Bir mali kayıt işlemi oluşturma

Bir mali kayıt işlemi, kayıt adımlarının sıralaması ve her bir adım için kullanılacak mali bağlayıcı grubu ile tanımlanır.

Mali kayıt süreci oluşturmak için bu adımları izleyin.

1. Commerce Headquarters'da **Mali kayıt süreci** sayfasına gidin (**Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali kayıt süreçleri**).
1. Her benzersiz mali kayıt süreci için yeni bir kayıt oluşturun.
1. Aşağıdaki adımları izleyerek işleme adımlarını kayıt edin:

    1. **Ekle**'yi seçin.
    1. Bir mali bağlayıcı türü seçin.
    1. **Grup numarası** alanında, uygun bir mali bağlayıcı grubu seçin.

### <a name="assign-entities-of-the-fiscal-registration-process-to-pos-profiles"></a>Mali kayıt işleminin varlıklarını POS profillerine atama

Mali kayıt işleminin varlıklarını POS profillerine atamak için bu adımları izleyin.

1. Commerce Headquarters'da **POS işlev profilleri** sayfasına gidin (**Retail ve Commerce \> Kanal kurulumu \> POS kutulumu \> POS profilleri \> İşlev profilleri**). 
1. Mali kayıt işlemini satış noktası işlev profiline atayın.
1. **Düzenle**'yi seçin ve sonra **Mali kayıt işlemi** sekmesinde, **İşlem numarası** alanında bir işlem seçin.
1. **Mali Hizmetler** sekmesinde, bağlayıcı yerleşim **Kaydı** ile bağlayıcı teknik profillerini seçin.
1. **POS donanım profili** sayfasında gidin (**Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> POS profilleri \> Donanım profilleri**).
1. Donanım profili için bağlayıcı teknik profilleri atayın. 
1. **Düzenle**'yi seçin ve **Mali çevre birimleri** sekmesinde bir satır ekleyin. 
1. **Profil numarası** alanında, bir bağlayıcı teknik profili seçin.
1. **Mali çevre birimleri** sekmesinde, bağlayıcı yerleşim **Donanım istasyonu** ile bağlayıcı teknik profillerini seçin.

> [!NOTE]
> Çok sayıda teknik profilleri, aynı donanım profiline ekleyebilirsiniz. Ancak, bir donanım profili veya POS işlevi profili herhangi bir mali bağlayıcı grubuyla yalnızca bir kesişime sahip olmalıdır.

Mali kayıt akışı mali kayıt işlemi ve mali tümleştirme bileşenlerinin bazı parametreleri tarafından tanımlanır: mali belge sağlayıcı için CRT eklentisi ve mali bağlayıcı için Donanım istasyonu eklentisi.

- Mali kayıt için etkinlik ve hareketlerin aboneliği mali belge sağlayıcısında önceden tanımlanmıştır.
- Mali belge sağlayıcısı, mali kayıt için kullanılan mali bağlayıcıları tanımlamaktan sorumludur. Mali kayıt işleminin geçerli adımı için bağlayıcı teknik profili ile POS'un eşleştirilmiş olduğu Donanım istasyonunun belirtilmiş olan bağlayıcı işlev profillerine Mali bağlayıcı için eşleşir.
- Mali belge sağlayıcısı, mali belge sağlayıcı yapılandırmasından veri eşleştirme ayarlarını kullanarak hareket/etkinlik verisini, örn. vergiler ve ödemeler gibi bilgileri bir mali belge oluşturulduğunda kullanır.
- Mali belge sağlayıcısı bir mali belge oluşturduğunda, mali belge bunu olduğu gibi mali cihaza gönderebilir veya bunu ayrıştırıp ve sonra cihaz API komut sırasına dönüştürebilir, iletişimin nasıl ele alındığına bağlı olarak.

### <a name="set-up-registers-with-fiscal-registration-restrictions"></a>Mali kayıt kısıtlamalarıyla kayıtları ayarlama

Mali kayda izin verilmeyen kayıtlar, örneğin ürün kataloğu arama, müşteri arama veya hareket taslağı oluşturma gibi yalnızca bu cihazlarda mali olmayan operasyonları sağlamanız gereken durumlarda, kayıtları seçebilirsiniz.

Mali kayıt kısıtlamalarıyla kayıtları ayarlamak için aşağıdaki adımları izleyin.

1. Commerce genel merkezinde, **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali kayıt işlemleri**'ne gidin.
1. Gerekli işlemi seçin.
1. **Mali işlem sınırlamalarına sahip POS kasaları** sekmesini seçin.
1. Mali işlem sınırlamalarına sahip kasaları gerektiği şekilde ekleyin.

### <a name="validate-the-fiscal-registration-process"></a>Mali kayıt işlemini doğrulama

Aşağıdaki durumlarda mali kayıt işlemini doğrulamanız önerilir:

- Yeni bir kayıt işlemi için tüm ayarları tamamladınız. Bu ayarlar, POS işlevsellik profillerine ve donanım profillerine kayıt işlemlerinin atanmasını içerir.
- Varolan bir mali kayıt işleminde değişiklikler yaptınız ve bu değişiklikler çalışma zamanında farklı bir mali bağlayıcının seçilememesine neden olabilir. (Örneğin, bir mali kayıt işlemi adımının bağlayıcı grubunu değiştirdiniz, bir bağlayıcı grubunda bir bağlayıcı işlev profili etkinleştirilmiş veya bağlayıcı grubuna yeni bir bağlayıcı işlev profili eklediniz.)
- Bağlayıcı teknik profillerin donanım profillerine atamasında değişiklikler yaptınız.

Mali kayıt sürecini doğrulamak için bu adımları izleyin.

1. Commerce Headquarters'da **Mali kayıt süreci** sayfasına gidin (**Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali kayıt süreçleri**).
1. Mali kayıt işlemini doğrulamak için **Doğrula** seçeneğini belirleyin.
1. **Dağıtım zamanlaması** sayfasında, **1070** ve **1090** işlerini veriyi kanal veritabanına aktarmak için kullanın.

## <a name="set-up-fiscal-texts-for-discounts"></a>İskontolar mali metinleri ayarlama

Bazı durumlarda, bir iskonto uygulandığında özel bir metnin mali giriş üzerine yazdırılması gerekir. İskontolar için mali metinleri **Mali bağlayıcı grubu** sayfasında (**Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali bağlayıcı grupları**) üzerinde ayarlayabilirsiniz.

- POS üzerinde uygulanacak el ile iskontolar için POS işlev profili içindeki **Ürün iskontosu** bilgi kodunda bilgi kodu veya bilgi kodu grubu için bir mali metin ayarlamalısınız.

    1. **Mali bağlayıcı grubu** sayfasında, **Mali giriş için metin**'i seçin.
    1. **Bilgi kodları** sekmesinde, **Ekle**'yi seçin ve bir bilgi kodu veya bilgi kodu grubu seçin.
    1. **Bilgi kodu numarası** alanında, bir değer seçin.
    1. **Alt kod numarası** alanında, seçilen bilgi kodu için bir alt kodun gerekli olması durumunda bir değer seçin.
    1. **Mali giriş için metin** alnında, mali girişe yazdırılacak bir mali metin belirleyin.
    1. **Kullanıcı girişini mali girişe yazdır** seçeneğini **Evet** olarak ayarlayarak mali girişteki metnin kullanıcının POS'ta yazdığı metin ile geçersiz kılınmasını sağlayın. Bu seçenek yalnızca **Metin** giriş türüne sahip bilgi kodları için geçerlidir.

    > [!NOTE]
    > Bilgi kodu gruplarının bağlantılı bilgi kodlarının ve tetiklenmiş bilgi kodlarının kullanıldığı senaryoları destekleyen çeşitli bilgi kodlarını belirtebilirsiniz. Bu senaryolarda, mali giriş, iskontonun uygulandığı hareket satırına bağlantılı tüm bilgi kodlarını içeren mali metni içerecektir.

- Kanala özel iskontolarda, iskonto kimliği için bir mali metin tanımlamalısınız.

    1. **Mali bağlayıcı grubu** sayfasında, **Mali giriş için metin**'i seçin.
    1. **İskontolar** sekmesinde, **Ekle**'yi seçin ve bir iskonto kimliği seçin.
    1. **Mali giriş için metin** alnında, mali girişe yazdırılacak bir mali metin belirleyin.

    > [!NOTE]
    > Birden fazla iskonto aynı hareket satırına uygulanıyorsa, mali metin bu iskonto satırıyla bağlantılı tüm mali metinleri içerecektir.

## <a name="set-error-handling-settings"></a>Hata işleme ayarlarını belirleme

Mali tümleştirme içinde kullanılabilen hata işleme seçenekleri, mali kayıt işleminde ayarlanır. Mali tümleştirme içindeki hata işleme hakkında daha fazla bilgi için bkz. [Hata işleme](fiscal-integration-for-retail-channel.md#error-handling).

Hata işleme ayarlarını ayarlamak için aşağıdaki adımları izleyin.

1. **Mali kayıt işlemi** sayfasında (**Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali kayıt işlemi**) üzerinde, mali kayıt işleminin her bir adımı aşağıdaki parametreleri ayarlayabilirsiniz.

    - **Atlamaya izin ver** – Bu parametre **Atla** seçeneğini hata işleme iletişim kutusuna etkinleştirir.
    - **Kaydedildiği şekilde işaretlemeye izin ver** - Bu parametre **Kaydedildi olarak işaretle** seçeneğini hata işleme iletişim kutusunda etkinleştirir.
    - **Ertelemeye izin ver** – Bu parametre **Ertele** seçeneğini hata işleme iletişim kutusuna etkinleştirir.
    - **Hata durumunda devam** – Bu parametre etkinleştirilmişse, mali kayıt işlemi POS kaydında mali kayıt veya bir hareket veya etkinlik başarısız olursa devam edebilir. Aksi taktirde, bir sonraki kayıt veya etkinliğin mali kaydını yürütmek için operatörün başarısız mali kaydı yeniden denemesi, atlaması veya hareketi veya etkinliği kaydedildi olarak işaretlemesi gerekir. Daha fazla bilgi için bkz [İsteğe bağlı mali kayıt](fiscal-integration-for-retail-channel.md#optional-fiscal-registration).

    > [!NOTE]
    > **Hatada devam et** parametresi etkinse, **Atlamaya izin ver** ve **Kaydedildi olarak işaretlenmeye izin ver** parametreleri otomatik olarak devre dışı bırakılır.

1. Hata işleme iletişim kutusundaki **Atla** ve **Kaydedildi olarak işaretle** seçenekleri, **Kaydı atlamaya izin ver veya kaydedildi olarak işaretle** izninin etkinleştirilmesini gerektirir. Bu izni etkinleştirmek için **İzin grupları** sayfasında (**Retail ve Commerce \> Personel \> İzin grupları**), **Kaydı atlamaya izin ver veya kaydedildi olarak işaretle** iznini **Evet** olarak ayarlayın.
1. Hata işleme iletişim kutusundaki **Ertele** seçeneği, **Ertelemeye izin ver** izninin etkinleştirilmesini gerektirir. İzni etkinleştirmek için **İzin grupları** sayfasında (**Retail ve Commerce \> Personel \> İzin grupları**), **Ertelemeye izin ver** iznini **Evet** olarak ayarlayın.
1. **Atla**, **Kaydedildi olarak işaretle** ve **Ertele** seçenekleri, operatörlerin mali kayıt başarısız olduğunda ek bilgiler girmesine olanak sağlar. Bu işlevi kullanılabilir kılmak için **Atla**, **Kaydedildi olarak işaretle** ve **Ertele** bilgi kodlarını bir mali bağlayıcı grubunda belirtmelisiniz. Operatörlerin girdiği bilgi, mali işleme bağlı bir bilgi kodu hareketi olarak kaydedilir. Bilgi kodları hakkında daha fazla bilgi için bkz. [Bilgi kodları ve bilgi kodu grupları](../info-codes-retail.md).

    > [!NOTE]
    > **Ürün** tetikleme işlevi, mali bağlayıcı gruplarındaki **Atla** ve **Kaydedildi olarak işaretle** için kullanılan bilgi kodlarında desteklenmemektedir.

    - **Mali bağlayıcı grubu** sayfasında, **Bilgi kodları** sekmesinde, bilgi kodlarını veya bilgi kodu gruplarını ve **Atla**, **Kaydedildi olarak işaretle** ve **Ertele** alanlarını seçin.

    > [!NOTE]
    > Bir mali belge ve bir mali olmayan belge, mali belge kayıt işleminin herhangi bir sayfasında oluşturulabilir. Bir mali belge sağlayıcısı eklentisi, her tür hareket veya etkinliği mali veya mali olmayan belgelere ilişkili olarak tanımlar. Hata işleme özelliği yalnızca mali belgeler için geçerlidir.
    >
    > - **Mali belge** - Başarıyla kaydedilmesi gereken zorunlu bir belge (örn. bir mali giriş).
    > - **Mali olmayan belge** - Hareket veya etkinlik için destekleyici bir belge (örn. bir hediye kartı fişi).

1. Bir sağlık denetimi hatası ortaya çıktıktan sonra operatörün güncel işlemi işlemeye devam etmesi (örneğin, bir hareketin oluşturulması veya sonlandırılması) için **Sağlık denetimi hatasını atlamaya izin ver** iznini **İzin grupları** sayfasından etkinleştirmeniz gerekir (**Retail ve Commerce \> Personeller \> İzin grupları**). Sağlık denetimi işlemi hakkında daha fazla bilgi için bkz. [Mali kayıt sağlık denetimi](fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

## <a name="set-up-fiscal-xz-reports-from-the-pos"></a>Mali X/Z raporlarını POS'tan ayarlamak

Mali X/Z raporlarının POS'tan çalıştırılmasını etkinleştirmek için bir POS düzenine yeni düğmeler eklemelisiniz.

- **Düğme kılavuzlar** sayfasında, [Düğme grubu tasarımcısını kullanarak POS düzenlerine POS işlemleri ekleme](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) içindeki talimatları kullanarak tasarımcıyı yükleyin ve bir POS düzenini güncelleştirin.

    1. Güncelleştirilecek düzeni seçin. 
    1. Yeni bir düğme ekleyin ve **Mali x yazdır** düğmesi özelliğini ayarlayın.
    1. Yeni bir düğme ekleyin ve **Mali Z yazdır** düğmesi özelliğini ayarlayın.
    1. **Dağıtım planlayıcısı** sayfasında **1090** işini çalıştırarak değişiklikleri kanal veritabanına aktarın.

## <a name="enable-manual-execution-of-postponed-fiscal-registration"></a>Ertelenen mali kaydın el ile yürütülmesini etkinleştir

Ertelenen mali kaydın el ile yürütülmesini etkinleştirmek için POS düzenine yeni bir düğme eklemelisiniz.

- **Düğme kılavuzlar** sayfasında, [Düğme grubu tasarımcısını kullanarak POS düzenlerine POS işlemleri ekleme](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) içindeki talimatları kullanarak tasarımcıyı yükleyin ve bir POS düzenini güncelleştirin.

    1. Güncelleştirilecek düzeni seçin.
    1. Yeni bir düğme ekleyin ve **Mali kayıt işlemini tamamla** düğmesi özelliğini ayarlayın.
    1. **Dağıtım planlayıcısı** sayfasında **1090** işini çalıştırarak değişikliklerinizi kanal veritabanına aktarın.


## <a name="view-connection-parameters-and-other-information-in-pos"></a>POS'taki bağlantı parametrelerini ve diğer bilgileri görüntüle

POS'taki bağlantı parametrelerini ve diğer bilgileri görüntülemek için aşağıdaki adımları izleyin.

1. Modern POS (MPOS) veya Bulut POS (CPOS) öğesini açın.
1. **Ayarlar**'ı seçin. Mali tümleştirme etkinleştirilmişse, sağdaki **Mali tümleştirme** bölümünde aşağıdaki bilgiler gösterilir:

    - Mali kaydın durumu
    - Son mali hareketin durumu
    - Bekleyen denetim olaylarının sayısı

1. Aşağıdaki bilgileri görüntülemek için **Ayrıntılar**'ı seçin:

    - Kayıt işlemi adımları
    - Bağlantı parametreleri
    - Denetim olayları ayrıntıları
 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
