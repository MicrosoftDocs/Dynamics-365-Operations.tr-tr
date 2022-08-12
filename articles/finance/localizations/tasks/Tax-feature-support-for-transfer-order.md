---
title: Transfer emirleri için vergi özelliği desteği
description: Bu makale, vergi hesaplama hizmeti kullanılarak transfer emirleri için yeni vergi özelliği desteğini açıklamaktadır.
author: Kai-Cloud
ms.date: 10/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b611abb2d68d93178d0c26ba40b22f1b8d26b191
ms.sourcegitcommit: 6d9fcb52d723ac5022a3002e0ced8e7b56e9bc2a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/27/2022
ms.locfileid: "9203124"
---
# <a name="tax-feature-support-for-transfer-orders"></a>Transfer emirleri için vergi özelliği desteği

[!include [banner](../../includes/banner.md)]

Bu makale, transfer emirlerinde vergi hesaplaması ve deftere nakil tümleştirmesi hakkında bilgi sağlar. Bu işlevsellik, stok transferleri için vergi hesaplamasını ayarlamanıza ve transfer emirlerine nakil yapmanıza olanak tanır. Avrupa Birliği (AB) katma değer vergisi (KDV) düzenlemeleri altında, stok transferleri topluluk içi tedarik ve topluluk içi alım olarak kabul edilir.

Bu işlevi yapılandırmak ve kullanmak için, üç ana adımı tamamlamanız gerekir:

1. **RCS'i ayarlama:** Regulatory Configuration Service, transfer emirlerinde vergi kodu belirleme için vergi özelliğini, vergi kodlarını ve vergi kodları uygulanabilirliğini ayarlayın.
2. **Dynamics 365 Finance'i ayarlama:** Finance'te, **Transfer emrinde vergi** özelliğini açın, stok için vergi hesaplama servis parametrelerini ayarlayın ve ana vergi parametrelerini ayarlayın.
3. **Stok ayarlama:** Transfer emri hareketleri için stok yapılandırmasını ayarlayın.

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a>Vergi ve transfer emri işlemleri için RCS'yi ayarlama

Bir transfer emrine dahil olan vergiyi ayarlamak için bu adımları izleyin. Burada gösterilen örnekte, Transfer emri, Hollanda'dan Belçika'ya yapılır.

1. **Vergi özellikleri** sayfasında, **sürümler** sekmesinde, taslak özelliğinin sürümünü seçin ve sonra **Düzenle**'yi seçin.

2. **Vergi özelliklerini ayarlama** sayfasında, **Vergi kodları** sekmesinde, yeni vergi kodları oluşturmak için **Ekle**'yi seçin. Bu örnekte, üç vergi kodu oluşturulur: **NL-Exempt**, **BE-RC-21** ve **BE-RC+21**.

    - Bir transfer emri Hollanda'daki bir ambardan sevk edildiğinde, Hollanda KDV'den muaf vergi kodu (**NL-Exempt**) uygulanır.
      
        **NL-Exempt** olarak oluşturun.
        1. **Ekle**'yi seçin, **Vergi kodu** alanına **NL-Exempt** yazın.
        2. **Vergi bileşeni** alanında **net tutara göre**'yi seçin.
        3. **Kaydet**'i seçin.
        4. **Ücret** sekmesinde **Ekle**'yi seçin.
        5. **Genel** bölümünde **Muaf**'ı **Evet** olarak belirleyin.
        6. **Muafiyet Kodu** alanına **EC** girin.

    - Belçika ambarında bir transfer emri alındığında, karşı ödeme mekanizması **BE-RC-21** ve **BE-RC+21** Vergi kodları kullanılarak uygulanır.
        
        Vergi kodu **BE-RC-21**'i oluşturun.      
        1. **Ekle**'yi seçin, **Vergi kodu** alanına **BE-RC-21** yazın.
        2. **Vergi bileşeni** alanında **net tutara göre**'yi seçin.
        3. **Kaydet**'i seçin.
        4. **Ücret** sekmesinde **Ekle**'yi seçin.
        5. **Vergi oranı** alanına **-21** girin.
        6. **Genel** bölümünde **Karşı Ödeme**'yi **Evet** olarak belirleyin.
        7. **Kaydet**'i seçin.
        
        Vergi kodu **BE-RC+21**'i oluşturun.
        1. **Ekle**'yi seçin, **Vergi kodu** alanına **BE-RC-21** yazın.
        2. **Vergi bileşeni** alanında **net tutara göre**'yi seçin.
        3. **Kaydet**'i seçin.
        4. **Ücret** sekmesinde **Ekle**'yi seçin.
        5. **Vergi oranı** alanına **21** girin.
        6. **Kaydet**'i seçin.

3. Vergi grubunu belirleyin.
    1. **Sütunları yönet**'i seçin ve sonra satır alanını **Vergi Grubu** seçin.
    2. **->** öğesini seçin ve ardından **Tamam**'ı seçin.
    3. Yeni bir vergi grubu eklemek için **Ekle**'yi seçin.
    4. **Vergi Grubu** sütununa, **AR-EU** girin ve sonra da **NL-Muafiyet** vergi kodunu seçin.
    5. Yeni bir vergi grubu eklemek için **Ekle**'yi seçin.
    6. **Vergi Grubu** sütununda, **RC-VAT** girin ve sonra da **BE-RC-21** ve **BE-RC+21** numaralı vergi kodlarını seçin.
4. Madde vergi grubunu belirleyin.
    1. **Sütunları yönet**'i seçin ve sonra satır alanını **Madde Vergi Grubu** seçin.
    2. **->** öğesini seçin ve ardından **Tamam**'ı seçin.
    3. Yeni bir madde vergi grubu eklemek için **Ekle**'yi seçin.
    4. **Madde Vergi Grubu** sütununda **TAM** yazın. **BE-RC-21**, **BE-RC+21** ve **NL-Muaf** vergi kodlarını seçin.
5. Vergi grubunun uygulanabilirliğini tanımlayın.

    1. **Sütunları Yönet**'i seçin ve sonra uygulanabilirlik tablosunu oluşturmak için kullanılacak sütunları seçin.

        > [!NOTE]
        > **İş süreci** ve **vergi yönleri** sütunlarını tabloya eklediğinizden emin olun. Transfer emirlerinde vergi işlevi için her iki sütun da gereklidir.

    2. Uygulanabilirlik kuralları ekleyin. **Vergi grubu** alanını boş bırakmayın.
        
        Transfer emri sevkiyatı için yeni bir kural ekleyin.
        1. **Uygulanabilirlik kuralları** sekmesinde **Ekle**'yi seçin.
        2. **İş süreci** alanında, kuralı transfer emri için uygulanabilir hale getirmek üzere **Stok**'u seçin.
        3. **Sevkiyatın yapıldığı ülke/bölge** alanına **NLD**'yi girin.
        4. **Sevkiyatın varacağı ülke/bölge** alanına **BEL**'yi girin.
        5. **Vergi yönü** alanında, kuralı transfer emri sevkiyatı için geçerli hale getirmek için **çıkış**'ı seçin.
        6. **Vergi Grubu** alanında, **AR-EU** öğesini seçin.
        
        Transfer emri girişi için başka bir kural ekleyin.
        
        1. **Uygulanabilirlik kuralları** sekmesinde **Ekle**'yi seçin.
        2. **İş süreci** alanında, kuralı transfer emri için uygulanabilir hale getirmek üzere **Stok**'u seçin.
        3. **Sevkiyatın yapıldığı ülke/bölge** alanına **NLD**'yi girin.
        4. **Sevkiyatın varacağı ülke/bölge** alanına **BEL**'yi girin.
        5. **Vergi yönü** alanında, kuralı transfer emri girişi için geçerli hale getirmek için **Giriş**'i seçin.
        6. **Vergi Grubu** alanında, **RC-VAT** öğesini seçin.

6. Madde vergi grubunun uygulanabilirliğini tanımlayın.

    1. **Sütunları Yönet**'i seçin ve sonra uygulanabilirlik tablosunu oluşturmak için kullanılacak sütunları seçin.
    2. Uygulanabilirlik kuralları ekleyin.
        
       > [!NOTE]
       > Vergilendirilebilir belge satırlarınızın varsayılan madde satış vergisi grubu zaten doğruysa, bu matrisi boş bırakın. 
        
        Transfer emri sevkiyatı ve makbuzu için yeni bir kural ekleyin.
        1. **Uygulanabilirlik kuralları** sayfasında **Ekle**'yi seçin.
        2. **İş süreci** alanında, kuralı transfer emri için uygulanabilir hale getirmek üzere **Stok**'u seçin.
        3. **Madde Vergi Grubu** alanında, **TAM** öğesini seçin.
7. Yeni vergi özelliği sürümünü tamamlayın ve yayımlayın.


## <a name="set-up-finance-for-transfer-order-transactions"></a>Transfer emri işlemleri için Finance'i ayarlama

Transfer emirleri için vergileri etkinleştirmek ve ayarlamak için bu adımları izleyin.

1. Finance'te, **Çalışma alanları** > **Özellik yönetimi**'ne gidin.
2. Listede, **transfer emrinde vergi** özelliğindeki vergiyi bulun ve seçin ve açmak için **şimdi etkinleştir**'i seçin.

    > [!IMPORTANT]
    > **Transfer emrinde vergi** özelliği vergi hesaplama servisine tamamıyla bağlıdır. Bu nedenle, yalnızca vergi hesaplama servisi yüklendikten sonra etkinleştirilebilir.

    ![Transfer emrinde vergi özelliği.](../media/image7.png)

3. Vergi hesaplama hizmetini etkinleştirin ve **Stok** iş sürecini seçin.

    > [!IMPORTANT]
    > Bu adımı, vergi hesaplama servisinin ve transfer emirlerinde vergi işlevinin kullanılabilir olmasını istediğiniz her tüzel kişilik için tamamlamalısınız.

    1. **Vergi** > **Kurulum** > **Vergi yapılandırması** > **Vergi hesaplama parametreleri**'ne gidin.
    2. **İş süreci** alanında **stok**'u seçin.

4. Karşı ödeme mekanizmasının ayarlandığını doğrulayın. **Genel Kayıt defteri** \> **Ayarlama** \> **Parametreler**'e gidin ve **Karşı ödeme** sekmesinde **Karşı ödemeyi etkinleştir** seçeneğinin **Evet** olarak ayarlandığını doğrulayın.

    ![Karşı ödeme seçeneğini etkinleştirme.](../media/image9.png)

5. İlgili vergi kodlarının, vergi gruplarının, madde vergi gruplarının ve KDV kayıt numaralarının vergi hesaplama servis kılavuzuna göre Finance'te ayarlandığını doğrulayın.
6. Bir geçiş transit hesabı ayarlayın. Bu adım yalnızca bir transfer emrine uygulanan vergi, vergi muafiyet veya karşı ödeme mekanizması için geçerli olmadığı durumlarda gereklidir.

    1. **Vergi** > **Kurulum** > **Satış vergisi** > **Genel muhasebe deftere nakil grupları**'na gidin.
    2. **Ara geçiş** alanında bir kayıt defteri hesabı seçin.

       ![Bir geçiş transit hesabı seçme.](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a>Transfer emri işlemleri için temel envanteri ayarlama

Transfer emri işlemlerini etkinleştirmek üzere temel envanteri ayarlamak için bu adımları izleyin.

1. Farklı ülkelerde veya bölgelerde ambarlarınız için sevk çıkış yeri ve sevk gidiş yeri siteleri oluşturun ve her tesis için birincil adresi ekleyin.

    1. **Ambar yönetimi** > **Kurulum** > **Ambar** > **Tesisler**'e gidin.
    2. Bir ambara daha sonra atayacağınız tesisi oluşturmak için **yeni**'yi seçin.
    3. Oluşturmanız gereken tüm diğer tesisler için 2. adımı yineleyin.

    > [!NOTE]
    > Oluşturduğunuz sitelerden biri **geçiş** olarak adlandırılmalıdır. Bu yordamın sonraki adımlarında, bu tesisi transit ambarına atayacaksınız böylece vergi ile ilgili stok fişleri transfer emirleri için "sevk etme" ve "teslim alma" işlemlerine nakledilebilecek. Transit tesisinin adresi vergi hesaplamasıyla ilgili değildir. Bu nedenle boş bırakabilirsiniz.

    ![Tesisleri ayarlama.](../media/image11.png)

2. Sevkiyat çıkış yeri, transit ve sevkiyat varış yeri ambarları oluşturun. Bir ambarda tutulan tüm adres bilgileri, vergi hesaplaması sırasında tesis adresini geçersiz kılar.

    1. **Ambar yönetimi** > **Ayarlama** > **Ambar** > **Ambarlar**'a gidin.
    2. Bir ambar oluşturmak için **Yeni**'yi seçin ve ilgili tesise atayın.
    3. Gerektiğinde her tesis için bir ambar oluşturmak üzere 2. adımı yineleyin.

       ![Ambar ayarlama.](../media/image12.png)

    > [!NOTE]
    > Sevkiyat çıkış yeri ambarı için, Transfer emri işlemleri için **transit ambarı** alanında bir transit ambarı seçilmelidir.
    >
    > ![Transit ambarı seçme.](../media/image13.png)

3. Transfer emri işlemleri için envanter deftere nakil yapılandırmasını ayarlayın.

    1. **Stok yönetimi** > **Ayarlama** > **Deftere nakil** > **Deftere nakil**'e gidin.
    2. **Stok** sekmesinde, bir kayıt defteri hesabının hem **stok sorunu** hem de **stok girişi** deftere nakli için ayarlandığını doğrulayın.

        ![Stok sorunu ve stok girişi deftere naklini ayarlama.](../media/image14.png)

    3. Kayıt defteri hesabının, **birimler arası borç** deftere nakil için ayarlandığını doğrulayın.

        ![Birimler arası borç deftere nakli ayarlama.](../media/image15.png)

    4. Kayıt defteri hesabının, **birimler arası alacak** deftere nakil için ayarlandığını doğrulayın.

        ![Birimler arası alacak deftere nakli ayarlama.](../media/image16.png)
        
        
  [!INCLUDE[footer-include](../../../includes/footer-banner.md)]
