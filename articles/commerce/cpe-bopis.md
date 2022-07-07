---
title: Dynamics 365 Commerce korumalı alan ortamında BOPIS'i yapılandırma
description: Bu makale; çevrimiçi satın al, mağazadan teslim al (BOPIS) işleminin, sağlandıktan sonra Microsoft Dynamics 365 Commerce korumalı alan ortamında nasıl yapılandırılacağını açıklar.
author: BrianShook
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 16cea7beb6ca05b5e96a9713b1217b414e27d56e
ms.sourcegitcommit: 252cb41c3029b623354698463f7b44a29fd9f184
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/15/2022
ms.locfileid: "9013197"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-sandbox-environment"></a>Dynamics 365 Commerce korumalı alan ortamında BOPIS'i yapılandırma

[!include [banner](includes/banner.md)]

Bu makale; çevrimiçi satın al, mağazadan teslim al (BOPIS) işleminin, ortam sağlandıktan sonra Microsoft Dynamics 365 Commerce korumalı alan ortamında nasıl yapılandırılacağını açıklar.

## <a name="prerequisite"></a>Önkoşul

Bu makaledeki yordamları yalnızca Commerce korumalı alan ortamınızı sağlandıktan ve yapılandırdıktan sonra tamamlayın. Ortamınızı sağlama ve yapılandırma hakkında bilgi için bkz. [Dynamics 365 Commerce korumalı alan ortamı sağlama](provisioning-guide.md) ve [Dynamics 365 Commerce korumalı alan ortamı yapılandırma](./cpe-post-provisioning.md).

Commerce ortamınız sağlandıktan ve uçtan uca yapılandırıldıktan sonra, bu makaleyi BOPIS senaryolarını etkinleştirmek için kullanabilirsiniz.

## <a name="configure-the-pos"></a>POS yapılandırma

### <a name="configure-modern-pos"></a>Modern POS yapılandırma

Kredi kartı ödemesi içeren BOPIS senaryoları bir donanım istasyonu gerektirir. Donanım istasyonu Windows ve Android istemcileri için Modern POS'a yerleşik olarak bulunur. iOS için Cloud POS veya Modern POS kullanıyorsanız, satış noktası (POS) istemcisi paylaşılan bir donanım istasyonuyla eşleştirilmelidir. Bu makale, Windows ve Android istemcileri için BOPIS'in nasıl yapılandırılacağını açıklamaktadır. Paylaşılan donanım istasyonu ayarlama hakkında daha fazla bilgi için bkz. [Retail hardware station'ı yapılandırma ve yükleme](./retail-hardware-station-configuration-installation.md).

1. **Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> Kasalar**'a gidin.
2. **SANFRAN-5** kasasını ve ardından **Düzenle**'yi seçin.
3. **HW002** olan **Donanım profili** alanının değerini **HW001** olarak değiştirin ve **Kaydet**'i seçin.
4. Değişiklikleri eşitlemek için **Retail ve Commerce \> Retail ve Commerce BT \> Dağıtım zamanlaması**'na gidin.
5. **1090** dağıtım zamanlamasını seçin ve ardından Eylem Bölmesinde **Şimdi çalıştır**'ı seçin.
6. Veri eşitlemeyi başlatmak için **Evet**'i ve sonra **Tamam**'ı seçin. 

### <a name="install-modern-pos"></a>Modern POS yükleme

1. **Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> Cihazlar**'a gidin.
2. **SANFRANCIS-5** cihazını seçin.
3. Eylem Bölmesinde, **İndir**'i ve sonra **Yapılandırma dosyası**'nı seçin.
4. **İndir**'i ve ardından **Retail Modern POS** öğesini seçin. 
5. **ModernPOSSetup.exe** dosyasının indirilmesi tamamlandığında **Dosyayı aç**'ı seçin.

    ![Dosya aç.](./dev-itpro/media/PAYMENTS/openfile.png)

6. Yükleme işlemine devam etmek için **İleri**'yi seçin. Yükleme tamamlandığında **Kapat**'ı seçin.

### <a name="activate-modern-pos"></a>Modern POS'u etkinleştirme

1. Windows masaüstünde, **Başlat** düğmesini seçin ve **Retail Modern POS** girin.
2. Etkinleştirmeyi başlatmak için **Retail Modern POS** uygulamasını seçin.
3. **Sonraki**'yi seçin. **Sunucu URL'si**, **Cihaz kodu** ve **Kayıt numarası** alanları, önceki yordamda karşıdan yüklediğiniz yapılandırma dosyasındaki bilgileri kullanarak önceden ayarlanmalıdır.
4. **Etkinleştir**'i seçin.
5. Bir kimlik doğrulama iletişim kutusu görüntülenir. Daha önce çalışan **000713-Andrew Collette** ile ilişkilendirilmiş olan e-posta adresini kullanan hesabı seçin.

    > [!NOTE]
    > Bir çalışanı kimliğinize henüz ilişkilendirmediyseniz, etkinleştirme başarısız olur. Bu durumda, [Dynamics 365 Commerce korumalı alan ortamını yapılandırma](cpe-post-provisioning.md#associate-a-worker-with-your-identity) makalesindeki "Çalışanı kimliğinizle ilişkilendirme" bölümünde anlatılan adımları izleyin.
    
6. Kuruluşunuzun cihazı yönetmesine izin vermek isteyip istemediğiniz sorulduğunda **Yalnızca bu uygulama**'yı seçin.
7. Etkinleştirme tamamlandığında **Başlarken**'i seçin.

### <a name="enable-bopis-in-modern-pos"></a>Modern POS'ta BOPIS'i etkinleştirme

1. Modern POS'ta operatör kodu olarak **000713** ve parola olarak **123** kullanarak oturum açın.
2. Tanıtıcı rehberlik videosu oynatılırken, iletişim kutusunun sol alt köşesindeki iki onay kutusunu işaretleyin ve ardından iletişim kutusunu kapatın.
3. Vardiyayı kapatmak isteyip istemediğiniz sorulmazda, sağdaki **Karşılama** sayfasına kaydırın,**Vardiyayı kapat**'ı seçin ve ardından POS'ta yeniden oturum açın.
4. Oturum açtıktan sonra, istendiğinde, **Çekmece işlemi olmayan bir işlem gerçekleştir** seçeneğini belirleyin.
5. **Karşılama** sayfasında sağa kaydırın ve **Donanım istasyonu seç** işlemini seçin.
6. **Yönet**'i seçin, **Donanım istasyonu kullan** seçeneğini **Açık** olarak ayarlayın ve **Tamam**'ı seçin.
7. POS oturumunu kapatın ve tekrar oturum açın.
8. Oturum açtıktan sonra **Yeni vardiya aç**'ı ve sonra **Çekmece**'yi seçin.

## <a name="complete-a-bopis-scenario"></a>BOPIS senaryosu tamamlama

### <a name="create-a-storefront-order-for-in-store-pickup"></a>Mağazadan alma için bir mağaza siparişi oluşturma

1. Ortam yapılandırması sırasında [e-Ticareti başlat](./provisioning-guide.md#initialize-e-commerce) adımında belirttiğiniz URL'ye gidin.
2. Bir madde seçin ve **Sepete ekle**'yi seçin.
3. Alışveriş çantası sayfasında, yeni eklediğiniz sipariş satır için **Bunu çek**'i seçin.
4. **Mağaza seç** iletişim kutusunda, **San Francisco** girin ve ardından **Ara** düğmesini seçin.
5. Sonuç listesinde, San Francisco mağazasını bulun ve **Buradan çek**'i seçin.
6. Alışveriş çantası sayfasında, **Misafir olarak ödeme yap**'ı seçin. 

    > [!NOTE]
    > Ödeme işlemine devam etmek için tanımlama bilgisi bildirimini kabul etmeniz gerekir. Bu bildirim, ödeme sayfasının en üstünde bir başlık olarak görünür.

7. Kredi kartı ödeme yöntemi için aşağıdaki ayrıntıları girin:

    - **Kart sahibi adı:** Herhangi bir ad girin.
    - **Kart numarası:** **4111-1111-1111-1111** girin.
    - **Son kullanma tarihi:** **10/20** girin.
    - **Kart doğrulama değeri (CVV) kodu:** **737** girin.

    > [!IMPORTANT]
    > Herhangi bir koşulda test sitesinde gerçek kredi kartı bilgilerini kullanmaya çalışmayın!

8. Fatura adresinin ayrıntılarını girerek ödeme işlemine devam edin ve **Kaydet ve devam et**'i seçin.
9. Sipariş verilmeye hazır olduğunda, **Ödeme**'yi seçin.

### <a name="synchronize-online-orders-to-the-back-office"></a>Çevrimiçi siparişleri arka ofisle eşitleme

Çevrimiçi siparişleri eşitleme hakkında bilgi için bkz. [Çevrimiçi satışları ve ödemeleri deftere nakletme](./tasks/posting-online-sales-payments.md).

### <a name="pick-up-an-order-in-the-store"></a>Bir siparişi mağazadan alma

1. POS'ta oturum açın.
2. **Karşılama** ekranında, **Sipariş karşılama**'yı seçin
3. Çekilecek madde listesinde, çevrimiçi olarak verilen siparişte bulunan satırı seçin.
4. Sipariş satırı seçiliyken, **Malzeme çek** öğesini seçin.

    Satır maddesi hareket ekranına eklenir ve vadesi gelen bakiye olarak **$0,00** görüntülenir.

5. **$0,00** tutarındaki vadesi gelen bakiyeyi seçin veya hareketi sonuçlandırmak için herhangi bir ödeme yöntemi seçin.

## <a name="troubleshooting"></a>Sorun giderme

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a>POS'ta alınan çevrimiçi siparişlerde sıfır olmayan bir bakiye bulunur

Bir sipariş mağazadan teslim alma için alındığında, ödenecek bakiye 0 (sıfır) değilse, Modern POS 'un kullanıldığından ve donanım istasyonunun etkin olduğundan emin olun. Bulut POS veya iOS için Modern POS kullanılıyorsa, paylaşılan bir donanım istasyonunun etkin olduğundan emin olun. Çevrimiçi olarak yapılan ödemeleri almak için bir çeşit etkin donanım istasyonu gerekir.

### <a name="general-issues-with-payment-capture"></a>Ödeme yakalamayla ilgili genel sorunlar

Tüm genel sorunlar için, her zaman öncelikle Modern POS veya İnternet Bilgi Hizmetleri (IIS) Hardware Station olay günlüklerine başvurmanız gerekir. Bu günlükleri, Windows olay günlüğünde aşağıdaki düğümlerde bulabilirsiniz:

- Uygulama ve Hizmet Günlükleri \> Microsoft \> Dynamics \> Commerce-ModernPOS
- Uygulama ve Hizmet Günlükleri \> Microsoft \> Dynamics \> Commerce-Hardware Station

## <a name="additional-resources"></a>Ek kaynaklar

[Dynamics 365 Commerce korumalı alan ortamını hazırlama](provisioning-guide.md)

[Dynamics 365 Commerce korumalı alan ortamı için isteğe bağlı özellikleri yapılandırma](cpe-optional-features.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure portalı](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce web sitesi](https://aka.ms/Dynamics365CommerceWebsite)

[Adyen ödeme bağlayıcısı](./dev-itpro/adyen-connector.md?tabs=8-1-3)

[Adyen bağlayıcısı ile çevrimiçi ödeme araçlarını kaydetme](./dev-itpro/adyen-connector-listpi.md)

[Çok yönlü kanal ödemelerine genel bakış](./omni-channel-payments.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
