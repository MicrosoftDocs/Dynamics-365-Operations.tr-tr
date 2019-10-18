---
title: Regression Suite Automation Tool eğitimi ayarlama ve yükleme
description: Bu konu,Regression Suite Automation Tool'un (RSAT). nasıl ayarlanacağını ve yükleneceğini gösteren bir eğitimdir.
author: kfend
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 50450669387f4e2c9e81975d5345c525c7929c47
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180657"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a>Regression Suite Automation Tool eğitimi ayarlama ve yükleme
Bu konu, RSAT ve RSAT kullanmayla ilgili araçları almanıza ve bu kurulumu başlatmanıza yardımcı olan bir eğitimdir. 

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Bu sayfayı PDF formatında karşıdan yükleyip kaydetmek için internet tarayıcısı araçlarını kullanın. 

## <a name="key-concepts"></a>Kilit kavramlar

- Regression Suite Automation Tool'u (RSAT) destekleyen çeşitli uygulamalar için gerekli olan yükleme ve önkoşul kurulumunu anlayın.
- Görev kaydedici özelliğinin Microsoft Dynamics Lifecycle Services (LCS) ve Microsoft Azure DevOps ile birlikte test çalıştırmalarını oluşturmanıza, yapılandırmanıza, çalıştırmanıza, araştırmanıza ve raporlamanıza nasıl olanak tanıdığını öğrenin.
- Görev kaydediciyi kullanarak iş görevlerini kaydetmek ve sonra görev kayıtlarını kaynak kodu yazmak zorunda kalmadan otomatik bir test paketine dönüştürmek için işlevsel kullanıcıları güçlendirin.

## <a name="before-you-begin"></a>Başlamadan önce

### <a name="prerequisites"></a>Önkoşullar

- Bu öğretici için Microsoft Dynamics 365 for Finance and Operations sürüm 10.0 (Nisan 2019) ya da sonraki bir sürümü çalıştıran bir ortam gereklidir. Microsoft Dynamics 365 for Finance and Operations Enterprise edition 7.3, Platform update 20 (PU20) ya da sonrasını kullanan müşteriler için desteklenmektedir.
- Kullanıcının ortamda yönetici hakları olmalıdır.
- Müşteri kiracı LCS'sine ve Azure DevOps'a (daha önce Microsoft Visual Studio Team Services \[VSTS\] olarak bilinen)sahip olmalısınız.
- Test paketleri oluşturan ve yöneten kullanıcının Azure DevOps Test Planları veya Test Yöneticisi lisansı olmalıdır. Aşağıdaki lisanslar Test Planlarına erişmenizi sağlar:
    - Visual Studio Kuruluş lisansı
    - Visual Studio Test Uzmanı lisansı
    - MSDN Platformları abone lisansı
- RSAT'ın bir web tarayıcısı aracılığıyla test ortamına erişimi olmalıdır.
- Test parametreleri oluşturmak ve düzenlemek için Microsoft Excel yüklü olmalıdır.

## <a name="configure-azure-devops"></a>Azure DevOps'ı yapılandır

### <a name="user-eligibility"></a>Kullanıcı uygunluğu

Kullanıcının Azure DevOps'da oluşturulduğundan ve Azure Test Planlarına erişim sağlayan bir abonelik düzeyine sahip olduğundan emin olun. Azure DevOps Test planı lisansının yalnızca, kullanıcının test çalışmalarını oluşturması ve yönetmesi gerekir (tüm RSAT kullanıcıları bu lisansı gerektirmez). Lisans gereksinimleri hakkında daha fazla bilgi için bkz.  [Lisans gereklilikleri](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements).

### <a name="create-a-new-azure-devops-project"></a>Yeni Azure DevOps projesi oluşturma
RSAT test çalışması için Azure DevOps, test paketi yönetimi, raporlama ve test olayı sonuçlarını araştırmaya yönelik kullanır. 

> [!NOTE]
> Varolan Azure DevOps projesini kullanabilirsiniz. Bununla birlikte, mevcut Azure DevOps projeniz özel bir şablona sahip olacak şekilde ayarlandıysa test olaylarını İş süreci modelleyiciden (BPM) Azure DevOps ile senkronize ettiğinizde "VSTS Senkronizasyon Hatası" hatası alırsınız (bkz. [BPM ile Azure DevOps eşitlemesini test etme](#test-the-synchronization-from-bpm-to-azure-devops) bölümü). Aşağıdaki en iyi uygulamalar özel şablon için kullanılıyorsa test olaylarını Azure DevOps'a eşitleyebilirsiniz. (Bu en iyi yöntemler hata iletisinde listelenmiştir.)

- Herhangi bir iş öğesi türünü veya kullanıma hazır alanı silmeyin.
- İş öğesi türüne ilişkin herhangi bir durumu silmeyin.
- İş öğesi türüne herhangi bir gerekli alan eklemeyin.

![En iyi yöntemler listesi ile ilgili hata iletisi](./media/setup_rsa_tool_02.png)

Aksi takdirde, bu öğreticide yeni bir Azure DevOps proje oluşturmanız önerilir. Daha fazla bilgi için bkz. [Özel bir Azure DevOps (VSTS) işlem şablonu kullanarak BPM ile eşitleme sorunları](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).

1. Azure DevOps URL'sini açma (`https://dev.azure.com/<Azure DevOps Name>`).
2. Azure DevOps sayfasının sağ üst köşesinde **Proje oluştur**'u seçin.

    ![Proje düğmesi oluşturma](./media/setup_rsa_tool_03.png)

3. Aşağıdaki alanları doldurun ve **Oluştur**'u seçin:

    - **Proje adı**
    - **Sürüm kontrolü** –  **Team Foundation Sürüm Kontrolü**nü seçin. **Git** varsayılan seçeneğinin desteklenmediğini unutmayın.
    - **İş maddesi süreci**

    ![Yeni proje iletişim kutusu oluştur](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a>Kişisel erişim belirteci oluşturma

Bu öğreticide, bir test durumu kitaplığı oluşturmak ve test olaylarınızı Azure DevOps ile eşitlemek için LCS İş Süreci Modelleyicisi'ni (BPM) kullanacaksınız. BPM ile Azure DevOps'u eşitlemek için kişisel erişim belirtecine ihtiyacınız olacak.

1. Azure DevOps projenize ait sayfanın sağ üst köşesinde bulunan profil simgesini seçin ve **Güvenlik**'i seçin.

    ![Güvenlik komutu](./media/setup_rsa_tool_05.png)

2. Sol bölmede, **Güvenlik** altında, **Kişisel erişim belirteçleri**'ni seçin. Sonra **Yeni belirteç**'i seçin.

    ![Kullanıcı ayarlarındaki kişisel erişim belirteçleri sekmesinde yeni belirteç düğmesi](./media/setup_rsa_tool_06.png)

3. Aşağıdaki alanları doldurun ve **Oluştur**'u seçin:

    - **Dosya Adı**
    - **Süre sonu (UTC)** – **Özel tanımlanmış** olarak seçeneği belirleyin ve sonra son kullanılabilir tarihi seçmek için tarih seçiciyi kullanın.
    - **Kapsamlar** - **Tam erişim** seçeneğini belirleyin.

    ![Yeni kişisel erişim belirteci iletişim kutusu oluşturma](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > Oluşturulan kişisel erişim belirtecini not edin. RSAT yapılandırmasını kurduğunuzda daha sonra ihtiyacınız olacaktır.

    ![Kişisel erişim belirteci](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a>LCS projesini yapılandırma

Ana test kitaplığınız için bir Lifecycle Services (LCS) projesi gerekir. İş Süreci Modelleyici (BPM) test durumlarınız için ana kitaplık olarak kullanılır. BPM, test kitaplıklarını LCS projeleri üzerinden yönetmek ve dağıtmak için kullanılır. Örneğin, bir Microsoft ortağı veya bağımsız yazılım satıcısı (ISV) oluşturma testi kitaplığı, test olayları BPM kitaplıkları biçiminde serbest bırakacaktır. BPM'de, test olayları iş sürecine göre düzenlenir. BPM, test geçişinin yürütme sırasını veya sıklığını tanımlamaz. Bu detaylar, bu konunun ilerisinde anlatıldığı gibi Azure DevOps'ta yönetilir.  

LCS projeniz için varolan bir müşteri uygulamasını veya ortak projeyi kullanabilirsiniz.

### <a name="update-the-lcs-language"></a>LCS dil kodunu güncelleştir

> [!NOTE]
> İş süreçlerini doğru şekilde göstermek üzere Kullanıcı arabirimi (UI) için, LCS tercih edilen dili **İngilizce (Amerika Birleşik Devletleri)** olarak ayarlanmalıdır.

1. LCS uygulama projesine gidin.
2. **Ayarlar** düğmesini (çark simgesi) sayfanın sağ üst köşesinde seçin ve sonra **Dil tercihleri**'ni seçin.

    ![Ayarlar menüsündeki komutlar](./media/setup_rsa_tool_09.png)

3. **Tercih edilen dil** alanında **İngilizce (Amerika Birleşik Devletleri)**'ni, seçin ve sonra **Kaydet**'i seçin.

    ![Kullanıcı ayarlarındaki dil tercihi sekmesi](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a>LCS'yi Azure DevOps projesine bağlanacak şekilde yapılandırın

Daha önce yeni bir Azure DevOps projesi oluşturduysanız LCS projesini bu projeye bağlanacak şekilde yapılandırın. Bunun dışındaki durumlarda, LCS projeniz Azure DevOps projenize zaten bağlıysa sonraki bölüme devam edebilirsiniz.

1. LCS uygulama projesine gidin.
2. **Menü** düğmesini seçin ve sonra **Proje ayarları**'nı seçin.

    ![Proje sunucu komutu](./media/setup_rsa_tool_11.png)

3. Sol bölmede **Visual Studio Team Services**'i seçin ve sonra **Setup Visual Studio Team Services**'i seçin.

    ![Proje ayarlarında Visual Studio Team Services sekmesi](./media/setup_rsa_tool_12.png)

4. **Azure DevOps sitesi URL'sinde** Azure DevOps sitesinin URL'sini girin. **Kişisel erişim belirteci** alanında, daha önce oluşturulmuş olan kişisel erişim belirtecini girin.

    > [!NOTE]
    > VSTS şimdi Azure DevOps olarak bilinmesine rağmen, LCS'yi Azure DevOps projenize bağlamak için eski URL'yi kullanın. Örneğin bu örnekte kullanılan Azure DevOps URL'si: `https://dev.azure.com/D365FOFastTrack/`. Ancak, aşağıdaki çizimde şu şekilde girilmiştir: `https://D365FOFastTrack.visualstudio.com/`.

    ![Kurulum adım 1 Visual Studio Team Services](./media/setup_rsa_tool_13.png)

5. **Devam**'ı seçin.
6. **Visual Studio Team Services projesi** alanında LCS projesiyle ilişkilendirmek için seçilen sitedeki VSTS projesini seçin. **Süreç şablonu** alanında **Çevik**'i varsayılan olarak ayarlayın. Özel bir şablon için [Yeni bir Azure DevOps projesi oluşturma](#create-a-new-azure-devops-project) bölümündeki en iyi yöntem kılavuzunu gözden geçirin. Sonra **Devam**'ı seçin.

    ![Kurulum adım 2 Visual Studio Team Services](./media/setup_rsa_tool_14.png)

7. Ayarlarınızı gözden geçirip **Kaydet**'i seçin.

    ![Kurulum adım 3 Visual Studio Team Services](./media/setup_rsa_tool_15.png)

8. Adınıza **Yapılandırılmış** Azure DevOps sitesine erişmek ve VSTS ile birleşen özellikleri açmak için LCS'yi yetkilendirmek üzere Yetkilendir'i seçin.

    ![Yetkilendir düğmesi](./media/setup_rsa_tool_16.png)

9. "Visual Studio Team Services'a sizin adınıza bağlanması için LCS'yi yetkilendirmek üzere harici bir siteye yönlendirilmek üzeresiniz. Devam edilsin mi?" sorusunu soracak bir mesaj kutusu görünür **Evet**'i seçin.

    ![İleti kutusu](./media/setup_rsa_tool_17.png)

10. **Kabul et**'i seçin.

    ![Erişim yetkilendiriliyor](./media/setup_rsa_tool_18.png)

11. Bir kullanıcı olarak yetkiniz varsa UI, LCS proje ayarları sayfasına dönmelisiniz.

    ![Yetkilendiren kullanıcı](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a>Yeni BPM kitaplığı oluştur

1. LCS uygulama projesine gidin.
2. **Menü** düğmesini seçin ve sonra **İş süreci modelleyici**'yi seçin.

    ![İş süreci modelleyici komutu](./media/setup_rsa_tool_20.png)

3. **Yeni kitaplık**'ı seçin.

    ![Yeni kitaplık oluştur düğmesi](./media/setup_rsa_tool_21.png)

4. **Kitaplık adı** alanına bir ad girin ve **oluştur**'u seçin. Bu öğretici için BPM kitaplığını **RSAT** olarak adlandırın.

    ![Yeni kitaplık iletişim kutusu oluşturma](./media/setup_rsa_tool_22.png)

5. Yeni **RSAT** BPM kitaplığını açın.
6. **Örnek Çekirdek İş Süreci** sürecini seçin ve sağ taraftaki **Düzenle**'yi seçin.

    ![Düzenleme modu düğmesi](./media/setup_rsa_tool_23.png)

7. Hem **Ad** alanını hem de **Açıklama** alanını **Ürün oluştur** olarak değiştirin. Sonra **Kaydet**'i seçin.

    ![Ad ve Açıklama alanları](./media/setup_rsa_tool_24.png)

## <a name="environment"></a>Ortam

### <a name="version-requirement"></a>Sürüm gereksinimi

Sürüm 10'un çalıştığı test veya korumalı alan ortamı gereklidir. 7.3, Platform update 20 (PU20) ya da sonrasını kullanan müşteriler için desteklenmektedir.

> [!NOTE]
> RSAT'ın bir web tarayıcısı aracılığıyla test ortamına erişimi olmalıdır.

### <a name="user-criteria"></a>Kullanıcı ölçütü

Kullanıcının bu ortamda yönetici hakları olmalıdır.

### <a name="set-up-help-settings-to-connect-with-lcs"></a>LCS ile bağlantı kurmak için yardım ayarlarını ayarlama

Bu adım, LCS ile ilgili olarak görev kayıtlarının istemci aracılığıyla LCS içindeki uygun BPM kitaplığına kaydedilebileceği şekilde bağlanmak için gereklidir.

1. İstemciyi açın.
2. **Sistem Yönetimi \> Kurulum \> Sistem parametreleri**'ne gidin.
3. **Yardım** sekmesinde **Lifecycle Services yardım yapılandırması** alanında ilgili LCS projesini (bu eğiticide**RSAT**) seçin.

    ![Yardım sekmesindeki Lifecycle Services Yardımı yapılandırma sekmesi](./media/setup_rsa_tool_25.png)

    BPM kitaplıkları uygun LCS projesi altında doldurulur.

4. **Kaydet**'i seçin.
5. Güncelleştirilmiş Yardım içeriğini görmek için tarayıcıyı yenilemeniz gerekebilir.

    ![Tarayıcıyı yenileme hakkında bildirim](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a>Görev kayıtları

> [!NOTE]
> Tüm görev kayıtlarınızın ana panoda göründüğünden emin olun. Tek kayıtların kısa kalmasını sağlayın ve satış siparişi oluşturma gibi bir iş görevine odaklanın.

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a>Görev kaydı oluşturma ve bunu BPM kitaplığına kaydetme

Yeni BPM kitaplığında oluşturulan basit iş sürecine ekleyebileceğiniz ilgili bir görev kaydı oluşturun.

1. İstemciyi açın.
2. Ana panoda **Ayarlar** düğmesini (çark simgesi) seçin ve sonra **Görev kaydedici**'yi seçin.

    ![Ayarlar menüsündeki komutlar](./media/setup_rsa_tool_27.png)

3. **Kayıt oluştur**'u seçin.

    ![Yeni kayıt oluşturma düğmesi](./media/setup_rsa_tool_28.png)

4. **Kayıt adı** ve **Kayıt açıklaması** alanlarını doldurun ve **Başlat**'ı seçin.

    ![Kayıt adı ve Kayıt açıklaması alanları](./media/setup_rsa_tool_29.png)

5. Ürün oluşturma adımlarını kaydedin. Bitirdiğinizde kaydı durdurmak için **Durdur**'u seçin.

    ![Bir ürün oluşturma adımları](./media/setup_rsa_tool_30.png)

6. **Lifecycle Services'e kaydet**'i seçin.

    ![Kaydetme seçenekleri](./media/setup_rsa_tool_31.png)

    Kitaplık bilgileri LCS'den yüklenir.

    ![İlerleme göstergesi](./media/setup_rsa_tool_32.png)

7. Görev kaydını ilişkilendirmek için BPM kitaplığını seçin. Bu öğretici için, yukarıda oluşturulmuş **RSAT** BPM kitaplığını seçin ve altında **Ürün oluşturma** iş sürecini seçin. Daha sonra **Tamam**'ı seçin.

    ![Görev kaydını bir BPM kitaplığıyla ve bir iş süreciyle ilişkilendirme](./media/setup_rsa_tool_33.png)

    Bir "Lifecycle Services'a başarıyla kaydedildi" iletisi görünür.

    ![LCS'ye başarılı bir kayıt ile ilgili ileti](./media/setup_rsa_tool_34.png)

8. Görev kaydını yerel olarak kaydetmek ve daha sonra LCS yoluyla BPM ile yüklemek istiyorsanız şu adımları izleyin:

    1. Kayıt tamamlandıktan sonra **Bu bilgisayara kaydet**'i seçin.

        ![Kaydetme seçenekleri](./media/setup_rsa_tool_35.png)

    2. Dosyayı yerel bilgisayarınıza kaydetmek için tarayıcının bildirim çubuğunda **Kaydet** veya **Farklı kaydet** seçeneğini belirleyin.

        ![Bildirim çubuğu](./media/setup_rsa_tool_36.png)

    3. **RSAT** BPM kitaplığına gidin ve görev kaydını kaydedeceğiniz iş sürecini seçin.
    4. **Genel** sekmesinde **Yükle**'yi seçin.

        ![Yükle düğmesi](./media/setup_rsa_tool_37.png)

    5. **Gözat**'ı seçin ve daha önce kaydettiğiniz .axtr dosyasını seçin. Sonra **Yükle**'yi seçin.

        ![Karşıya yüklenecek. axtr dosyasını seçme](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a>BPM ile Azure DevOps eşitlemesini test etme

Bir görev kaydı iş sürecine iliştirildiğinde, (sırasıyla) LCS'deki VSTS eşitleme özelliğini kullanarak iş işleminin ve ilişkili görev kaydının özellik ve test olayı Azure DevOps olarak eşitlenebildiğini doğrulamanız gerekir.

> [!NOTE]
> ' Azure DevOps'ta oluşturulan ilgili iş öğesi türü, LCS projesini Azure DevOps'ta yapılandırdığınızda yeni [Yeni bir Azure DevOps projesi oluşturma](#create-a-new-azure-devops-project) bölümünde açıklandığı gibi seçtiğiniz işlem şablonuna bağlı olarak değişir.

1. BPM kitaplığına gidin ve daha önce oluşturduğunuz **RSAT** kitaplığını açın.
2. Üç nokta düğmesini (**...**) ve **VSTS Eşitleme** öğesini seçin.

    ![Üç nokta menüsünde VSTS eşitleme komutu](./media/setup_rsa_tool_39.png)

    VSTS eşitleme işlemi tamamlandıktan sonra sol tarafta**Gereksinimler** sekmesi görünür ve bu, ilgili Azure DevOps iş öğesini içerir.

    > [!NOTE]
    > Azure DevOps'ta oluşturulan iş öğesi başlığı ön eki olarak BPM kitaplığının adına sahip olacaktır.

    ![Gereksinimler sekmesi](./media/setup_rsa_tool_40.png)

3. Sayfayı yenileyin.
4. Üç nokta düğmesini (**...**) Ek bir seçenek olan **Test olaylarını eşitle**'de göreceksiniz. Bu seçeneği seçin.

    ![Üç nokta menüsünde test olaylarını eşitle menüsü](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > **Test olaylarını eşitle** sayfayı yeniledikten sonra da açılmıyorsa BPM için ana sayfaya gidin ve tüm kitaplık için **Test olaylarını eşitle**'yi seçin. Böylece, tüm kitaplık için eşitlemeyi etkili şekilde zorlarsınız.
    > 
    > ![Tüm kitaplık için test olaylarını Eşitlemeyi seçme](./media/setup_rsa_tool_42.png)

    Test olaylarını eşitlemeyi tamamlandıktan sonra **Gereksinimler** sekmesinde yeni bir test olayı oluşturulur.

    ![Gereksinimler sekmesinde yeni test olayı](./media/setup_rsa_tool_43.png)

5. Azure DevOps projenize gidin ve  **Panolar \> Çalışma Maddeleri**'ni seçin.

    ![Panolar altında Çalışma Maddeleri komutu](./media/setup_rsa_tool_44.png)

6. BPM eşitlemesi aracılığıyla oluşturduğunuz iş öğesinin ve test olayının varolduğunu doğrulayın.

    ![İş maddesi ve test olayı](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a>RSAT'ı yükleme ve Yapılandırma

RSAT, Windows 10 çalıştıran ve ortama bir web tarayıcısı üzerinden bağlanabilen herhangi bir bilgisayara kurulabilir (Internet Explorer ya da Google Chrome).

> [!NOTE]
> Aracın yeni bir sürümünü yüklemeden önce önceki sürümü kaldırmanızı öneririz.

### <a name="install-an-authentication-certificate"></a>Kimlik doğrulama sertifikası yükleme

Kimlik doğrulamayı etkinleştirmek için, RSAT'ın çalıştığı bilgisayara bir sertifika oluşturmanız ve yüklemeniz gerekir.

#### <a name="generate-a-certificate"></a>Yeni bir sertifika oluşturma

1. Sertifika dosyası oluşturmak için, bir Microsoft Windows PowerShell penceresini yönetici olarak açın ve aşağıdaki komutu çalıştırın.

    ```
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. **Çalıştır** iletişim kutusuna **certlm.msc** girerek sertifika yöneticisini açın ve **Kişisel \> Sertifikalar**'ın altındaki **D365 Otomatik test sertifikası** sertifikasını onaylayın.

    > [!NOTE]
    > Sertifikalar yerel bilgisayarda depolandığından **certmgr.msc** değil **certlm.msc** yazdığınızdan emin olun.

    ![D365 otomatik test sertifikası sertifikası](./media/setup_rsa_tool_46.png)

3. Sertifikada sağa tıklayın ve sonra **Kopyala**'yı seçin.
4. **Güvenilen Kök Sertifika Yetkilileri \> Sertifikalar**'a gidin.

    ![Güvenilen Kök Sertifika Yetkilileri klasörü altındaki sertifikalar klasörü](./media/setup_rsa_tool_47.png)

5. **Eylem** menüsünde sertifikayı **Güvenilen Kök Sertifika Yetkilileri** konumuna yapıştırmak için **Yapıştır**'ı seçin.

    ![Yapıştır komutu Eylem menüsü](./media/setup_rsa_tool_48.png)

6. Boşluk veya özel karakterler olmadan yüklü sertifikanın parmak izini almak için bir Windows PowerShell penceresini yönetici olarak açın ve aşağıdaki komutları çalıştırın.

    ```
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > Daha sonra Uygulama Nesne Sunucusu (AOS) için .wif dosyalarını güncelleştirdiğinizde ve RSAT yapılandırmasını kurduğunuzda bu dosyaya ihtiyacınız olacağından parmak izini kaydedin.

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a>AOS bilgisayarını bağlantıya güvenecek şekilde yapılandırın

> [!NOTE]
> Ortam bir katman 2 + ortamıysa ortam için **Tüm** AOS bilgisayarları için wif.config dosyasında sertifika parmak izi güncelleştirilmelidir.

1. AOS bilgisayarına bir Uzaktan Masaüstü Protokolü (RDP) bağlantısı kurun. Oturum açma ayrıntıları LCS içindeki ortam ayrıntıları sayfasında bulunabilir.
2. Microsoft Internet Information Services'i (IIS) açın ve site listesinde **AOSService**'i bulun.

    ![Siteler listesinde AOSService](./media/setup_rsa_tool_49.png)

3. **\<Sürücü\>: \\AosService\\WebRoot** dosyasını açmak için **Keşfet**'e sağ tıklayın. **wif.config** dosyasını bulun.

    ![WebRoot klasöründe wif.config dosyası](./media/setup_rsa_tool_50.png)

4. Aşağıdaki örnekte gösterildiği gibi, **wif.config** dosyasını sertifikanız ve yetki adınız için yeni bir yetki girişi ekleyerek günceştirin.

    ```
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > Birden fazla kullanıcı aynı uygulamayı kullanıyorsa her kullanıcı ayrı parmak izleri oluşturmalı ve bu parmak izlerinin her biri **\<anahtarlar\>** bölümüne eklenmelidir.

5. Birden fazla AOS bilgisayarı varsa her ek bilgisayar için 3. ile 4. adımları yineleyin.

    > [!NOTE]
    > Eski katman 2 ortamlarından farklı olarak yeni katman 2 ortamları iki AOS örneğiyle dağıtılır.

6. Tüm AOS bilgisayarlarında **iisreset**'i çalıştırın.

    > [!NOTE]
    > Bir katman 1 bilgisayarında **iistreset**'i çalıştırmak için yönetici haklarına sahip değilseniz LCS içindeki ortam ayrıntıları sayfasında, Yönet > Yeniden başlat hizmetlerini seçin.

#### <a name="tier-2-environment"></a>Katman 2+ ortamı

Katman 2 + (Standart kabul testi sanal alanı veya daha ileri) ortamı kullanılıyorsa RSAT'ın yüklendiği bilgisayarda aşağıdaki kayıt defteri ayarını doğrulayın veya ayarlayın. Bu adım, kimlik doğrulama veya RSAT bağlantı hatalarından kaçınmanıza yardımcı olacağından gereklidir.

```
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a>RSAT öğesini yükle

1. <https://www.microsoft.com/download/details.aspx?id=57357>'a gidin ve **İndir**'i seçin.
2. Tüm dosyaları seçin ve sonra **İleri**'yi seçin.

    ![Tüm dosyalar seçiliyor](./media/setup_rsa_tool_51.png)

3. Yükleyiciyi çalıştırmak için .msi paketine çift tıklayın. Yükleme tamamlandığında **Son**'u seçin.

    ![RSAT Yükleyici dosyası](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a>Selenium ve tarayıcı sürücülerini yükleme

RSAT'ın eski sürümlerinde, Selenium ve Tarayıcı sürücülerini yüklemeniz gerekiyordu. Bu sürücüleri, otomatik olarak yüklendiğinden yüklemeniz artık gerekmez.

1. RSAT'ı ilk açışınızda, Selenium'u otomatik olarak karşıdan yükleyip kurmanız istenir. Daha fazla bilgi için [Configure RSAT](#configure-rsat) bölümüne bakın.
2. Bir test olayını çalıştırabilmeniz için, RSAT yapılandırmasında seçilen varsayılan tarayıcıya karşılık gelen tarayıcı sürücüsünü otomatik olarak karşıdan yükleyip kurmanız istenir. Daha fazla bilgi için [Test çalışmalarını yükleme ve çalıştırma](#load-and-run-test-cases) bölümüne bakın.

## <a name="get-started-with-rsat"></a>RSAT kullanmaya başlama

### <a name="create-a-test-plan-and-test-suites"></a>Test planı ve test paketleri oluşturma

1. Azure DevOps projesine gidin ve **Test Planları**'nı seçin.

    ![Test planları komutu](./media/setup_rsa_tool_53.png)

2. **Yeni Test Planı**'nı seçin.

    ![Yeni Test Planı düğmesi](./media/setup_rsa_tool_54.png)

3. **Ad** alanını doldurun ve sonra **Oluştur**'u seçin. Bu öğretici için test planını **RSAT test planı** olarak adlandırın.

    ![Yeni Test Planı iletişim kutusu](./media/setup_rsa_tool_55.png)

4. Artı işaretini (**+**) seçin ve sonra yeni test planı altında **Statik paket** oluşturmak için statik paketi seçin. Yeni test paketini **T01 – Stoka Aktar** olarak adlandırın.

    > [!NOTE]
    > Ayrıca, yeni test olaylarını BPM'den otomatik olarak RSAT test paketine çekilmesini istiyorsanız sorgu tabanlı bir paket oluşturabilirsiniz.

    ![Statik bir paket oluşturma](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a>Test paketlerine test olayları iliştirme

1. Test paketine varolan test olaylarını eklemek için sağ taraftan **Varolanı ekle**'yi seçin.

    ![Varolan faaliyeti ekleme düğmesi](./media/setup_rsa_tool_57.png)

2. **Pakete test olaylarını ekle** sayfasında **Sorguyu çalıştır**'ı seçin, ve sonra test paketine eklenecek test olayını seçin. Bu eğitici için, **Yeni bir ürün oluştur** test olayı seçeneğini belirleyin. Sonra sayfanın sağ alt köşesindeki **Test olayları ekle**'yi seçin (Bu düğme aşağıdaki çizimde gösterilmez).

    ![Sorgu çalıştırma düğmesi](./media/setup_rsa_tool_58.png)

    Test olayı **T01-Stoka Aktar** test paketine eklenir.

    ![Test paketine eklenen test olayı](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a>RSAT konfigüre et

1. RSAT'ı açın.

    ![RSAT simgesi](./media/setup_rsa_tool_60.png)

2. The Regression Suite Automation Tool'un Selenium gerektirdiğini, şimdi otomatik olarak karşıdan yükleyip kurmak isteyip istemediğinizi belirten bir uyarı iletisi mi alıyorsunuz? **Evet**'i seçin.

    ![Uyarı iletisi](./media/setup_rsa_tool_61.png)

3. Sağ üst köşedeki **Ayarlar** düğmesini (çark sembolü) seçin ve sonra görünen iletişim kutusunda aşağıdaki alanları doldurun:

    - **Azure DevOps Url** – Azure DevOps projenizin `https://yourAzureDevOpsUrlHere.visualStudio.com` gibi URL'sini girin.
    - **Erişim Belirteci** – Aracın Azure DevOps'a bağlanmasını sağlayan erişim belirtecini girin. Bu öğreticide daha önce oluşturduğunuz kişisel erişim belirtecini kullanın. Daha fazla bilgi için bkz. [Kişisel erişim belirteçleriyle erişimi doğrulama](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).
    - **Proje Adı** – Azure DevOps projenizin adını seçin.
    - **Test planı** - Test olaylarınızı içeren Azure DevOps test planını seçin. Daha fazla bilgi için bkz. [Test planları ve test paketleri oluşturma](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan). Test planı seçtikten sonra Azure DevOps bağlantınızı test etmek için **test bağlantısı**'nı seçin.
    - **Ana bilgisayar adı** – Test ortamının ana bilgisayar adını **\<myaos\>.cloudax.dynamics.com** örneğindeki gibi girin. **https://** ya da **http://** öneki eklemeyin.
    - **SOAP Ana bilgisayar Adı** – Test ortamının SOAP ana bilgisayar adını girin. Genellikle, SOAP ana bilgisayar adı ana bilgisayar adıyla aynıdır, ancak **soap** soneki vardır. Örnek: **\<myaos\>soap.cloudax.dynamics.com**. **https://** ya da **http://** öneki eklemeyin.

        > [!NOTE]
        > Ana bilgisayar adını ve SOAP ana bilgisayar adını bulmak için, IIS Yöneticisini açın, **Siteler \> AOSService**'e sağ tıklayın **Bağlama düzenleme**'yi seçin. **Ana bilgisayar adı** sütunundaki değerler, size ana bilgisayar adı ve SOAP ana bilgisayar adı verir (SOAP ana bilgisayar adı URL'de son ek **SOAP**'ye sahiptir).

        ![Ana makine adı sütununda ana bilgisayar adı ve SOAP ana bilgisayar adı](./media/setup_rsa_tool_63.png)

    - **Yönetici kullanıcı adı** – Test ortamında bir yönetici kullanıcısının e-posta adresini girin.
    - **Parmak izi** – Bu öğreticide daha önce anlatıldığı şekilde, kimlik doğrulama sertifikasının parmak izini girin.
    - **Çalışma dizini** – Excel test veri dosyaları gibi test otomasyon dosyalarını depolamak için klasör konumunu belirtin. Örneğin, **C:\\Temp\\RegressionTool** girin veya seçin.

        > [!NOTE]
        > Klasörün adında boşluk varsa klasör bulunamadığı için yürütme işlemi başarısız olur. Bu sorun bilinen bir sorundur ve aracın en son sürümünde düzeltilmelidir.

    - **Varsayılan tarayıcı** – ya **Internet Explorer** ya da **Google Chrome**'u seçin. Uygun tarayıcı sürücülerinin yüklenmiş olduğundan emin olun.
    - **Test çalıştırması zaman aşımı** – test çalıştırmaları için zaman aşımı süresini dakika cinsinden belirtin. Zaman aşımı süresi geçtiğinde, tüm etkin pencereler kapatılır ve bekleyen test olayları başarısız olur.
    - **Test eylemi zaman aşımı** – bu alan, Finance and Operations ortamı sunucu istekleri için zaman aşımı süresini dakika cinsinden denetler. Genellikle varsayılan değer (2 dakika) yeterli olmalıdır. Ancak, daha yavaş ortamlarda, zaman aşımları ile ilgili hatalar oluşursa bu değeri arttırmak isteyebilirsiniz.
    - **Şirket adı** – Excel parametre dosyaları oluşturulurken varsayılan şirket olarak kullanılacak şirket adını girin. Şirketi daha sonra Excel parametre dosyasını düzenleyerek değiştirebilirsiniz.

    ![Ayarlar iletişim kutusu](./media/setup_rsa_tool_62.png)

4. Ayarlarınızı uygulamak ve kaydetmek için **Uygula**'yı seçin.

    Geçerli ayarlarınızı bilgisayarınızdaki bir yapılandırma dosyasına kaydetmek için **Farklı kaydet**'i seçin. Geçerli ayarlarınızı bilgisayarınızdaki bir yapılandırma dosyasına geri yüklemek için **Aç**'ı seçin.

5. İletişim kutusunu kapatmak için **Kapat**'ı seçin.

### <a name="load-and-run-test-cases"></a>Test çalışmalarını yükleme ve çalıştırma

1. Azure DevOps projesinden **RSAT Test Planı**'nı yüklemek için **Yükle**'yi seçin.

    ![Yükle düğmesi](./media/setup_rsa_tool_64.png)

2. **Yeni bir ürün oluştur** test olayını test paketinden seçin ve sonra **Yeni \> Test Yürütmesi ve Parametresi dosyalarını oluştur**'u seçin.

    ![Yeni menüde Test Yürütmesi ve Parametre Dosyaları oluştur komutu](./media/setup_rsa_tool_65.png)

    Excel parametre dosyası, RSAT yapılandırmasında belirttiğiniz yerel klasörde oluşturulur. (örneğin **C:\\Temp\\RegressionTool**).

    ![Oluşturulan Excel parametre dosyası](./media/setup_rsa_tool_66.png)

3. Parametre dosyalarını kaydetmek istiyorsanız **Yükle**'yi seçin. Tüm seçili test olaylarının test otomasyon dosyaları, ileride kullanılmak üzere Azure DevOps'a yüklenir. (Bu dosyalar Excel test parametre dosyalarını içerir.)

    Bu şekilde parametre dosyalarını (ve otomasyon dosyalarını) test olayından doğrudan Azure DevOps konumundan yüklemek için **Yükle**'yi seçebilirsiniz. Parametre dosyalarını yeniden oluşturmak zorunda değilsiniz. Değişiklikleri parametre dosyasında tutmak ve bunların üzerine yazılmasını istemiyorsanız bu yaklaşım daha sonra da önemli olacak.

4. Otomasyon dosyalarının ve Azure DevOps parametre dosyalarının kaydedildiğini doğrulamak için Azure DevOps projesine gidin,**Panolar \> İş Maddesi**'ni seçin ve **Yeni ürün oluştur** test olayını seçin. **Ekler** sekmesinde dört dosya görmelisiniz:

    - **.cs** – C\# otomasyon dosyası
    - **. dll** – Derleme olarak derlenen otomasyon dosyası
    - **.xlsx** – Excel parametre dosyası
    - **.xml** – Kayıt dosyası

    ![Ekler sekmesindeki dosyalar](./media/setup_rsa_tool_67.png)

5. Çalıştırılacak test olayını seçin ve sonra **Çalıştır**'ı seçin.

    > [!NOTE]
    > Test olaylarını çalıştırmadan önce tarayıcı olarak Internet Explorer kullanıyorsanız **Windows Görüntü Ayarları \> Ölçek ve Düzen**'in **%100** olduğundan emin olun. Bu ayarı bir sanal makinede (VM) değiştirmek istemezseniz VM'ye erişmeye çalıştığınız istemci (dizüstü bilgisayar) üzerinde bunu değiştirin. Böylece, çözünürlük ayarları VM görüntü ayarları tarafından devralınır.

    ![Masaüstü çözünürlüğü %100 olarak ayarlandı](./media/setup_rsa_tool_68.png)

6. Tarayıcı sürücüleri sistemde yüklü değilse "Bu işlem \<tarayıcı adı\> sürücüsü gerektirir. Şimdi otomatik olarak karşıdan yükleyip kurmak istiyor musunuz?" uyarısı alacaksınız. **Evet**'i seçin.

    ![Internet Explorer için uyarı iletisi](./media/setup_rsa_tool_69.png)

    ![Chrome için uyarı iletisi](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > Tarayıcı olarak Chrome kullanıyorsanız ve Chrome sürümü doğru olmadığı için oturumun oluşturulmadığını bildiren bir hata iletisi alıyorsanız en son Chrome sürücüsünü <http://chromedriver.chromium.org/downloads> **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Ortak\\Dış\\Selenium** dosyasına indirin.

    ![Chrome için hata uyarısı iletisi](./media/setup_rsa_tool_71.png)

    Test olayı çalıştırılır ve **Sonuç** alanı güncellenir.

    ![İlerleme göstergesi](./media/setup_rsa_tool_72.png)

    Bu öğreticiyi yazıldığı gibi izlediyseniz **Ürün oluşturmak için görev kaydı** ürün adını sabit kodlanmış değer olarak kaydetmediği için, yeni ürün test olayı oluşturma başarısız olacaktır. Aynı test olayını yeniden çalıştırırsanız ürün zaten varolduğu için bir hata iletisi almalısınız.

    ![Sonuç alanı Başarısız olarak ayarlandı](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a>Test sonuçlarını görüntüleme

1. Başarısız test çalışmasına çift tıklayın.

    Hata iletisi alırsınız.

    ![Hata iletisi](./media/setup_rsa_tool_73.png)

2. Hata iletisinin tamamını görüntülemek için **Ayrıntıları** seçin.

    ![Tüm hata iletisi](./media/setup_rsa_tool_74.png)

3. Hata iletisinin ayrıntılı bir sürümünü Azure DevOps'ta görüntülemek için **Azure DevOps'da Aç**'ı seçin. Azure DevOps'ta, test olayının durumunu ve ayrıntılı hata iletisini görebilirsiniz.

    ![Azure DevOps'ta ayrıntılı hata iletisi](./media/setup_rsa_tool_75.png)

4. Azure DevOps test sonuçlarını doğrudan proje içinde görüntülemek için,**Test Planları \> Test Planları \> Çalıştır**'a gidin. Daha fazla ayrıntı görmek istediğiniz test olayına çift tıklayın.

    ![Azure DevOps'ta test çalışmalarının listesi](./media/setup_rsa_tool_76.png)

5. **Çalıştırma özeti** sekmesi test olayının başarısız olduğunu gösterir, ancak gerçek hata iletisini sağlamaz. Ayrıntılı hata iletisini görüntülemek için **Test sonuçları** sekmesini seçin.

    ![Çalıştırma özeti sekmesi](./media/setup_rsa_tool_77.png)

    **Test sonuçları** sekmesi, sonuç ve hata iletisiyle birlikte test olayı bilgilerini sağlar.

    ![Test sonuçları sekmesi](./media/setup_rsa_tool_78.png)

6. Ayrıntılı hata iletisini görüntülemek için ilgili kayda çift tıklayın.

    ![Ayrıntılı hata iletisi](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > Tüm hata iletileri yerel olarak **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**'te de bulunur.

7. Test olayı sonuçlarını, **Dışa aktar**'ı seçerek test planı düzeyinden de dışa aktarabilirsiniz.

    ![Test planını dışa aktarma](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a>Excel parametre dosyasını değiştirme

1. RSAT'ı açın.
2. Test olayını seçin ve sonra Excel parametre dosyasını açmak için **Düzenle**'yi seçin.

    **EcoResProductCreate** tablosunda, **Ürün numarası** alanı değerinin sabit kodlanmış olduğuna dikkat edin. Test olayını yeniden çalıştırmadan önce bu alanı yeni bir ürün numarasıyla güncelleştirmelisiniz.

3. Excel parametre dosyasını yeniden açmak ve her seferinde ürün numarasını el ile güncelleştirmek zorunda kalmadan her çalışma için benzersiz bir ürün numarası oluşturmak için aşağıdaki Excel formülünü kullanın.

    ```
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > **Genel** sekmesine ek olarak the Excel parametre dosyası, test olayının ziyaretlerinin her form sayfası için bir veri sekmesi içerir.

    ![Ürün numarası dosyası](./media/setup_rsa_tool_81.png)

4. **Kaydet**'i seçip Excel .çalışma sayfasını kapatın.
5. Excel parametre dosyasını Azure DevOps'a kaydetmek için **Yükle**'yi seçin.

    ![İleti yükleme başarılı](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > Test olaylarını belirli bir kullanıcı bağlamında çalıştırmak için, kullanıcının e-posta kodunu Excel parametre dosyasının **Genel** sekmesindeki **Test Kullanıcısı** alanına girin. RSAT'ın en son sürümünde, Excel parametre dosyasındaki alanların düzeni güncelleştirildi, ancak kavram aynı kaldı.
    >
    > ![Test Kullanıcısı alanı](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a>Sonuçları doğrulama

- Test olayını yeniden çalıştırmak için **Çalıştır**'ı seçin ve test olayının geçtiğini doğrulayın. Test sonuçlarını, [View the test results](#view-the-test-results)'ta tanımlandığı gibi görüntüleyebilirsiniz.

    ![Sonuç alanı Başarılı olarak ayarlandı](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a>Test olaylarının zincirlenmesi

RSAT'ın en önemli özelliklerinden biri test olaylarının zincirlenmesidir (bir başka deyişle, bir testin diğer testlere geçiş yeteneği). Test olayları, Azure DevOps test planındaki tanımlı sıralara göre çalıştırılır. (Bu sıra test aracının kendisinde de güncelleştirilebilir.) Bu nedenle, değişkenleri bir test olayından diğerine geçirmek istiyorsanız testlerin doğru sırada olması çok önemlidir.

Bu bölümde, ilk test olayında bir kaydedilmiş değişken oluşturacak, ikinci bir test olayı yaratmayacak ve kaydedilmiş değişkeni ilk test olayından ikinci test olayına geçireceksiniz. Daha sonra test olaylarını RSAT'da zincirleme bir test olayı olarak çalıştırırsınız.

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a>Kaydedilmiş bir değişken oluşturmak için varolan görev kaydını değiştirme

1. İstemciyi açın.
2. **Ayarlar** düğmesini (çark simgesi) seçin ve sonra **Görev kaydedici**'yi seçin.
3. **Kaydı Düzenle**'yi seçin.

    ![Kaydı Düzenle düğmesi](./media/setup_rsa_tool_85.png)

4. **Lifecycle Services'tan Aç**'ı seçin.

    ![Lifecycle Services'tan aç düğmesi](./media/setup_rsa_tool_86.png)

5. **Lifecycle Services kitaplığı**'nı seçin.

    ![Lifecycle Services kitaplığını seç düğmesi](./media/setup_rsa_tool_87.png)

    BPM kitaplıkları LCS'den yüklenir.

    ![İlerleme göstergesi](./media/setup_rsa_tool_88.png)

6. BPM kitaplıkları LCS'den yüklendikten sonra **RSAT** BPM kitaplığını seçin ve görev kaydının ilişkilendirildiği **Yeni bir ürün oluştur** iş süreci oluşturun. Daha sonra **Tamam**'ı seçin.

    ![BPM kitaplığı ve iş süreci seçme](./media/setup_rsa_tool_89.png)

7. Uygun görev kaydının adı **Kayıt adı** alanına girilir. **Başlat**'ı seçin.

    ![Kayıt adı alanına görev kaydı için benzersiz bir ad girin.](./media/setup_rsa_tool_90.png)

8. **Ürün bilgileri yönetimi \> Ürünler**'e gidin ve **Ürün oluştur**'un kaydedildiği orijinal görev kaydetmede **Yeni**'yi seçin.
9. **Adım ekle**'yi seçin.

    > [!NOTE]
    > Yeni adım, bölmesinde seçtiğiniz adımdan **sonra** eklenir.

    ![Adım ekle düğmesi](./media/setup_rsa_tool_91.png)

10. **Ürün numarası** alanına sağ tıklayın ve sonra **Görev kaydedici \> Kopyala**'yı seçin.

    ![Komutu kopyalama](./media/setup_rsa_tool_92.png)

11. Yeni adım bölmeye eklenir. Daha sonra gereksinim duyacağınız **Ürün numarası** alanındaki değeri not edin.

    ![Yeni adım eklendi](./media/setup_rsa_tool_93.png)

12. **Düzenlemeyi bitir**'i seçin.
13.  **Save to Lifecycle Services**'e kaydeti seçin ve yeni görev kaydını, özgün görev kaydının ilişkilendirildiği aynı BPM kitaplığıyla ve iş süreciyle ilişkilendirin. Daha fazla bilgi için [Görev kaydı oluşturma ve bunu BPM kitaplığına kaydetme](#create-a-task-recording-and-save-it-to-the-bpm-library)bölümüne bakın.
14. BPM kitaplığına gidin ve **Test olaylarını eşitle**'yi [BPM ile Azure DevOps eşitlemesini test etme](#test-the-synchronization-from-bpm-to-azure-devops) bölümünde açıklandığı gibi Azure DevOps'a iliştirin.
15. RSAT'ı açın ve test paketindeki tüm test olaylarını yeniden yüklemek için **Yükle**'yi seçin. Test olayını seçerek ve [Test olaylarını yükleme ve çalıştırma](#load-and-run-test-cases) bölümünde açıklandığı gibi **Yeni \> Test Yürütme ve Parametre dosyaları**'nı seçerek uygun test olayı için otomasyon ve parametre dosyalarını yeniden oluşturmalısınız.

    > [!NOTE]
    > Excel parametre dosyası açık bırakılırsa yeniden oluşturma işlemi başarısız olur. Bu nedenle, yeni Excel parametre dosyasını oluşturmadan önce test olayı için Excel parametre dosyasının kapalı olduğundan emin olun.

16. Yeni Excel parametre dosyasını açmak için **Düzenle**'yi seçin. Çevrimiçi 9 yeni bir **Kaydedilmiş değişken** girişi göreceksiniz. Bu değişken **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, görev kaydının XML dosyasına kaydedilir ve sonraki testlerde kullanılabilir.

    ![Kaydedilen değişken girişi](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a>Yeni bir test olayı oluşturma

1. **RSAT** BPM kitaplığına gidin.
2. **Örnek Desteği İş Süreci** sürecini seçin ve sağ taraftaki **Düzenle**'yi seçin.
3. Hem **Ad** alanını hem de **Açıklama** alanını **Ürünü serbest bırak** olarak değiştirin. Sonra **Kaydet**'i seçin.

    ![Ad ve açıklama bir ürünü serbest bırakmak için değişti](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a>Doğrulama işlevi olan yeni bir görev kaydı oluşturma

- Daha önce USRT tüzel kişiliği tarafından oluşturulan ürünü serbest bırakmak için bir görev kaydı oluşturun. Daha fazla bilgi için [Görev kaydı oluşturma ve bunu BPM kitaplığına kaydetme](#create-a-task-recording-and-save-it-to-the-bpm-library)bölümüne bakın.

    > [!NOTE]
    > Zincirleme test olayları için, *alan değerini el ile yazarak* gereksinim duyduğunuz kaydı bulmanız veya filtreleyerek her zaman önerilir. Bu şekilde, söz konusu eylem, sonraki test olayında dikkate alınması gereken kaydı belirleyebilir.

    ![Doğrulama işlevi olan yeni bir görev kaydı](./media/setup_rsa_tool_96.png)

    Yukarıdaki resimde gösterildiği gibi ürün Quick Filter'la bulunduktan sonra ancak **Ürünleri serbest bırak**'ı seçmeden önce, **Ürün numarası** alanının değerini doğrulamak için ürün kimliğinin daha önce oluşturulmuş ürün kimliği olduğundan emin olun. Değeri doğrulamak için **ürün numarası** alanına sağ tıklayın ve **Görev kaydedici \> Doğrula \> Geçerli Değer**'i seçin.

    ![Geçerli kaydı doğrulama](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a>Görev kaydetmeyi BPM'e kaydetme

1. Görev kaydı tamamlandıktan sonra **Lifecycle Services'e kaydet**'i seçin.

    ![Kaydetme seçenekleri](./media/setup_rsa_tool_98.png)

2. Kitaplık bilgileri LCS'den yüklenir.

    ![İlerleme göstergesi](./media/setup_rsa_tool_99.png)

3. Görev kaydını ilişkilendirmek için BPM kitaplığını seçin. Bu öğretici için, yukarıda oluşturulmuş **RSAT** BPM kitaplığını seçin ve altında **Ürünü serbest bırakma** iş sürecini seçin. Daha sonra **Tamam**'ı seçin.

#### <a name="sync-bpm-to-azure-devops"></a>BPM'i Azure DevOps ile eşitleme

1. BPM kitaplığına gidin ve **RSAT** kitaplığını açın.
2. **VSTS eşitleme**'yi seçin ve sonra **Test olaylarını eşitle**'yi seçin. Daha fazla bilgi için [BPM ile Azure DevOps eşitlemesini test etme](#test-the-synchronization-from-bpm-to-azure-devops) bölümüne bakın.

    Eşitleme tamamlandıktan sonra yeni iş maddesi ve **Bir ürünü serbest bırakma**'ya karşılık gelen test olayı **Panolar \> İş Maddeleri**'ndeki .Azure DevOps'da görünür

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a>Varolan test paketine yeni test çalışmasını ekleme

1. **Test planları \> Test planları**'na gidin ve **RSAT Test Planı** planını seçin.
2. **Varolanı ekle**'yi seçin.
3. **Test olaylarını pakete ekle** sayfasında **Sorguyu çalıştır**'ı seçin.
4. **Bir ürünü serbest bırakmak** için oluşturulan yeni test olayını seçin ve sonra sayfanın sağ alt köşesinde **Test olayları ekle**'yi seçin (Bu düğme aşağıdaki çizimde gösterilmez).

    ![Paket sayfasına test durumları ekleme](./media/setup_rsa_tool_100.png)

    Test paketinin şimdi iki test olayı vardır.

    ![Test paketinin şimdi iki test olayı var](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a>RSAT'a test olaylarını yükleme

1. RSAT'ı açın ve **Yükle**yi seçin.
2. Test olayları yüklenir ve "Bu eylem Excel test veri dosyalarının üzerine yazacak, yerel değişikliklerin kaybolmasına neden olacak. Devam etmek istiyor musunuz?" yazan bir uyarı alacaksınız Excel parametresi dosyalarını yerel sistemde güncelleştirmek ama Azure DevOps'a yüklenen Excel parametre dosyalarını güncelleştirmemek için **Evet**'i seçin.

    ![Uyarı iletisi](./media/setup_rsa_tool_102.png)

    Her iki test olayı da, ilk test olayı için Excel parametre dosyası ile birlikte yüklenir. Son çalıştırmada karşıya **Yükle**'yi seçtiğinizden, parametre dosyaları Azure DevOps'tan çekilir .

    ![Test senaryoları yüklendi](./media/setup_rsa_tool_103.png)

3. Yalnızca ikinci test olayını seçin ve sonra  **Yeni \> Test Yürütmesi ve Parametre Dosyaları oluştur**'u seçin.

#### <a name="edit-the-excel-parameter-file"></a>Excel parametre dosyasını düzenleme

1. Yalnızca ikinci test olayını seçin ve sonra karşılık gelen Excel parametre dosyasını açmak için **Düzenle**'yi seçin.
2. Kaydedilmiş değişken **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**'yi ilk test olayından ürün numarasının kullanıldığı tüm alanlara kopyalayın ([Kaydedilmiş bir değişken oluşturmak için varolan görev kaydını değiştirme](#modify-an-existing-task-recording-to-create-a-saved-variable) bölümüne bakın). Bu durumda, değişkeni **Ürün numarasına** ve **Ürün Numarasını Doğrula** alanlarını **EcoResProductListPage** sayfasına kopyalarsınız.

    ![Ürün numarası ve ürün numarası doğrulama alanları](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > Değişkenler, yalnızca aynı test olayı sırasında testler arasında geçirilebilir. Değişkenlerin adlarının tam olarak eşleşmesi gerekir.

3. **Kaydet**'i seçip Excel .çalışma sayfasını kapatın.
4. Excel parametre dosyasında yaptığınız değişiklikleri kaydetmek için **Yükle**'yi seçin.

#### <a name="run-the-chained-test-cases"></a>Zincirleme test olaylarını çalıştırma

1. Çalıştırılacak iki test olayını da seçin ve sonra **Çalıştır**'ı seçin.
2. Her iki test olayının da geçtiğini doğrulayın.

    ![Her iki test çalışması için de sonuç alanı geçildi](./media/setup_rsa_tool_105.png)
