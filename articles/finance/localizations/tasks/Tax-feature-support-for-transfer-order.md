---
title: Transfer emirleri için vergi özelliği desteği
description: Bu konu, vergi hesaplama servisi kullanılarak transfer emirleri için yeni vergi özelliği desteğini açıklamaktadır.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1c47c327841b8c712220e440e2aa6b4fe2b31b4a1ccd03dc0a200dbeb7394071
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721701"
---
# <a name="tax-feature-support-for-transfer-orders"></a>Transfer emirleri için vergi özelliği desteği

[!include [banner](../../includes/banner.md)]

Bu konu, transfer emirlerinde vergi hesaplaması ve deftere nakil tümleştirmesi hakkında bilgi sağlar. Bu işlevsellik, stok transferleri için vergi hesaplamasını ayarlamanıza ve transfer emirlerine nakil yapmanıza olanak tanır. Avrupa Birliği (AB) katma değer vergisi (KDV) düzenlemeleri altında, stok transferleri topluluk içi tedarik ve topluluk içi alım olarak kabul edilir.

Bu işlevi yapılandırmak ve kullanmak için, üç ana adımı tamamlamanız gerekir:

1. **RCS'i ayarlama:** Regulatory Configuration Service, transfer emirlerinde vergi kodu belirleme için vergi özelliğini, vergi kodlarını ve vergi kodları uygulanabilirliğini ayarlayın.
2. **Finance'i ayarlama:** Microsoft Dynamics 365 Finance'te, **Transfer emrinde vergi** özelliğini açın, stok için vergi servis parametrelerini ayarlayın ve ana vergi parametrelerini ayarlayın.
3. **Stok ayarlama:** Transfer emri hareketleri için stok yapılandırmasını ayarlayın.

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a>Vergi ve transfer emri işlemleri için RCS'yi ayarlama

Bir transfer emrine dahil olan vergiyi ayarlamak için bu adımları izleyin. Burada gösterilen örnekte, Transfer emri, Hollanda'dan Belçika'ya yapılır.

1. **Vergi özellikleri** sayfasında, **sürümler** sekmesinde, taslak özelliğinin sürümünü seçin ve sonra **Düzenle**'yi seçin.

    ![Düzenle'yi seçme.](../media/tax-feature-support-01.png)

2. **Vergi özelliklerini ayarlama** sayfasında, **Vergi kodları** sekmesinde, yeni vergi kodları oluşturmak için **Ekle**'yi seçin. Bu örnekte, üç vergi kodu oluşturulur: **NL-Exempt**, **BE-RC-21** ve **BE-RC+21**.

    - Bir transfer emri Hollanda'daki bir ambardan sevk edildiğinde, Hollanda KDV'den muaf vergi kodu (**NL-Exempt**) uygulanır.
      
        **NL-Exempt** olarak oluşturun.
        1. **Ekle**'yi seçin, **Vergi kodu** alanına **NL-Exempt** yazın.
        2. **Vergi bileşeni** alanında **net tutara göre**'yi seçin.
        3. **Kaydet**'i seçin.
        4. **Ücret** sekmesinde **Ekle**'yi seçin.
        5. **Genel** bölümünde **Muaf**'ı **Evet** olarak değiştirin.

        ![NL-Vergi muafiyet kodu.](../media/tax-feature-support-02.png)

    - Belçika ambarında bir transfer emri alındığında, karşı ödeme mekanizması **BE-RC-21** ve **BE-RC+21** Vergi kodları kullanılarak uygulanır.
        
        Vergi kodu **BE-RC-21**'i oluşturun.      
        1. **Ekle**'yi seçin, **Vergi kodu** alanına **BE-RC-21** yazın.
        2. **Vergi bileşeni** alanında **net tutara göre**'yi seçin.
        3. **Kaydet**'i seçin.
        4. **Ücret** sekmesinde **Ekle**'yi seçin.
        5. **Vergi oranı** alanına **-21** girin.
        6. **Genel** bölümünde **Karşı Ödeme**'yi **Evet** olarak değiştirin.
        7. **Kaydet**'i seçin.

        ![Ters giderler için BE-RC-21 vergi kodu.](../media/tax-feature-support-03.png)
        
        Vergi kodu **BE-RC+21**'i oluşturun.
        1. **Ekle**'yi seçin, **Vergi kodu** alanına **BE-RC-21** yazın.
        2. **Vergi bileşeni** alanında **net tutara göre**'yi seçin.
        3. **Kaydet**'i seçin.
        4. **Ücret** sekmesinde **Ekle**'yi seçin.
        5. **Vergi oranı** alanına **21** girin.
        6. **Kaydet**'i seçin.

        ![Ters giderler için BE-RC+21 vergi kodu.](../media/tax-feature-support-04.png)

3. Vergi kodlarının uygulanabilirliğini tanımlayın.

    1. **Sütunları Yönet**'i seçin ve sonra uygulanabilirlik tablosunu oluşturmak için kullanılacak sütunları seçin.

        > [!NOTE]
        > **İş süreci** ve **vergi yönleri** sütunlarını tabloya eklediğinizden emin olun. Transfer emirlerinde vergi işlevi için her iki sütun da gereklidir.

    2. Uygulanabilirlik kuralları ekleyin. **Vergi kodları**, **vergi grubu** ve **Madde vergi grubu** alanlarını boş bırakmayın.
        
        Transfer emri sevkiyatı için yeni bir kural ekleyin.
        1. **Uygulanabilirlik kuralları** sekmesinde **Ekle**'yi seçin.
        2. **İş süreci** alanında, kuralı transfer emri için uygulanabilir hale getirmek üzere **Stok**'u seçin.
        3. **Sevkiyatın yapıldığı ülke/bölge** alanına **NLD**'yi girin.
        4. **Sevkiyatın varacağı ülke/bölge** alanına **BEL**'yi girin.
        5. **Vergi yönü** alanında, kuralı transfer emri sevkiyatı için geçerli hale getirmek için **çıkış**'ı seçin.
        6. **Vergi kodları** alanında **NL-Exempt**'i seçin.
        7. **Vergi grubu** alanına ve **Madde vergi grubu** kısmına, Finance sisteminizde tanımlanan ilgili satış vergisi grubunu ve madde satış vergisi grubunu girin.
        
        Transfer emri girişi için başka bir kural ekleyin.
        1. **Uygulanabilirlik kuralları** sekmesinde **Ekle**'yi seçin.
        2. **İş süreci** alanında, kuralı transfer emri için uygulanabilir hale getirmek üzere **Stok**'u seçin.
        3. **Sevkiyatın yapıldığı ülke/bölge** alanına **NLD**'yi girin.
        4. **Sevkiyatın varacağı ülke/bölge** alanına **BEL**'yi girin.
        5. **Vergi yönü** alanında, kuralı transfer emri girişi için geçerli hale getirmek için **Giriş**'i seçin.
        6. **Vergi kodları** alanında **BE-RC+21** ve **BE-RC-21**'i seçin.
        7. **Vergi grubu** alanına ve **Madde vergi grubu** kısmına, Finance sisteminizde tanımlanan ilgili satış vergisi grubunu ve madde satış vergisi grubunu girin.

        ![Uygulanabilirlik kuralları.](../media/image5.png)

4. Yeni vergi özelliği sürümünü tamamlayın ve yayımlayın.

    [![Yeni sürümün durumunu değiştirme.](../media/image6.png)](../media/image6.png)

## <a name="set-up-finance-for-transfer-order-transactions"></a>Transfer emri işlemleri için Finance'i ayarlama

Transfer emirleri için vergileri etkinleştirmek ve ayarlamak için bu adımları izleyin.

1. Finance'te **Çalışma alanları** \> **Özellik yönetimi**'ne gidin.
2. Listede, **transfer emrinde vergi** özelliğindeki vergiyi bulun ve seçin ve açmak için **şimdi etkinleştir**'i seçin.

    > [!IMPORTANT]
    > **Transfer emrinde vergi** özelliği vergi servisine tamamıyla bağlıdır. Bu nedenle, yalnızca vergi Servisi yüklendikten sonra etkinleştirilebilir.

    ![Transfer emrinde vergi özelliği.](../media/image7.png)

3. Vergi hizmetini etkinleştirin ve **Stok** iş sürecini seçin.

    > [!IMPORTANT]
    > Bu adımı, vergi servisinin ve transfer emirlerinde vergi işlevinin kullanılabilir olmasını istediğiniz her tüzel kişilik için tamamlamalısınız.

    1. **Vergi** \> **Ayarlama** \> **Vergi yapılandırması** \> **Vergi servis ayarı**'na gidin.
    2. **İş süreci** alanında **stok**'u seçin.

    ![İş süreci alanını ayarlama.](../media/image8.png)

4. Karşı ödeme mekanizmasının ayarlandığını doğrulayın. **Genel Kayıt defteri** \> **Ayarlama** \> **Parametreler**'e gidin ve **Karşı ödeme** sekmesinde **Karşı ödemeyi etkinleştir** seçeneğinin **Evet** olarak ayarlandığını doğrulayın.

    ![Karşı ödeme seçeneğini etkinleştirme.](../media/image9.png)

5. İlgili vergi kodlarının, vergi gruplarının, madde vergi gruplarının ve KDV kayıt numaralarının vergi servis kılavuzuna göre Finance'te ayarlandığını doğrulayın.
6. Bir geçiş transit hesabı ayarlayın. Bu adım yalnızca bir transfer emrine uygulanan vergi, vergi muafiyet veya karşı ödeme mekanizması için geçerli olmadığı durumlarda gereklidir.

    1. **Vergi** \> **Ayarlama** \> **Satış vergisi** \> **Genel muhasebe deftere nakil grupları**'na gidin.
    2. **Ara geçiş** alanında bir kayıt defteri hesabı seçin.

    ![Bir geçiş transit hesabı seçme.](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a>Transfer emri işlemleri için temel envanteri ayarlama

Transfer emri işlemlerini etkinleştirmek üzere temel envanteri ayarlamak için bu adımları izleyin.

1. Farklı ülkelerde veya bölgelerde ambarlarınız için sevk çıkış yeri ve sevk gidiş yeri siteleri oluşturun ve her tesis için birincil adresi ekleyin.

    1. **Ambar yönetimi** \> **Kurulum** \> **Ambar** \> **Tesisler** öğesine gidin.
    2. Bir ambara daha sonra atayacağınız tesisi oluşturmak için **yeni**'yi seçin.
    3. Oluşturmanız gereken tüm diğer tesisler için 2. adımı yineleyin.

    > [!NOTE]
    > Oluşturduğunuz sitelerden biri **geçiş** olarak adlandırılmalıdır. Bu yordamın sonraki adımlarında, bu tesisi transit ambarına atayacaksınız böylece vergi ile ilgili stok fişleri transfer emirleri için "sevk etme" ve "teslim alma" işlemlerine nakledilebilecek. Transit tesisinin adresi vergi hesaplamasıyla ilgili değildir. Bu nedenle boş bırakabilirsiniz.

    ![Tesisleri ayarlama.](../media/image11.png)

2. Sevkiyat çıkış yeri, transit ve sevkiyat varış yeri ambarları oluşturun. Bir ambarda tutulan tüm adres bilgileri, vergi hesaplaması sırasında tesis adresini geçersiz kılar.

    1. **Ambar yönetimi** \> **Ayarlama** \> **Ambar** \> **Ambarlar**'a gidin.
    2. Bir ambar oluşturmak için **Yeni**'yi seçin ve ilgili tesise atayın.
    3. Gerektiğinde her tesis için bir ambar oluşturmak üzere 2. adımı yineleyin.

    ![Ambar ayarlama.](../media/image12.png)

    > [!NOTE]
    > Sevkiyat çıkış yeri ambarı için, Transfer emri işlemleri için **transit ambarı** alanında bir transit ambarı seçilmelidir.
    >
    > ![Transit ambarı seçme.](../media/image13.png)

3. Transfer emri işlemleri için envanter deftere nakil yapılandırmasını ayarlayın.

    1. **Stok Yönetimi** \> **Ayarlama** \> **Deftere nakil** \> **Deftere nakil** sayfasına gidin.
    2. **Stok** sekmesinde, bir kayıt defteri hesabının hem **stok sorunu** hem de **stok girişi** deftere nakli için ayarlandığını doğrulayın.

        ![Stok sorunu ve stok girişi deftere naklini ayarlama.](../media/image14.png)

    3. Kayıt defteri hesabının, **birimler arası borç** deftere nakil için ayarlandığını doğrulayın.

        ![Birimler arası borç deftere nakli ayarlama.](../media/image15.png)

    4. Kayıt defteri hesabının, **birimler arası alacak** deftere nakil için ayarlandığını doğrulayın.

        ![Birimler arası alacak deftere nakli ayarlama.](../media/image16.png)
