---
title: Uygulama sınıfı yöntemlerini çağırmak için ER ifadeleri tasarlama
description: Bu makalede, gerekli uygulama sınıfları yöntemlerini çağırarak Elektronik raporlama yapılandırmalarında mevcut uygulama mantığının nasıl yeniden kullanılabileceği açıklanmaktadır.
author: kfend
ms.date: 11/02/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21c24cee15e9a0fd11838b5b8fd816e4aaed9a93
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267857"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a>Uygulama sınıfı yöntemlerini çağırmak için ER ifadeleri tasarlama

[!include [banner](../../includes/banner.md)]

Bu makalede, ER ifadelerinde gerekli uygulama sınıfları yöntemlerini çağırarak [Elektronik raporlama (ER)](../general-electronic-reporting.md) yapılandırmalarında mevcut uygulama mantığının nasıl yeniden kullanılabileceğiyle ilgili bilgiler sağlanmaktadır. Çağırma sınıfları için bağımsız değişken değerleri çalışma zamanında dinamik olarak tanımlanabilir. Örneğin, değerler ayrıştırılmasını sağlamak için, ayrıştırma belgesindeki bilgileri temel alabilir.

Örneğin bu makalede, bir uygulamanın veri güncelleştirmesi için gelen banka ekstrelerini ayrıştırmak üzere bir işlem tasarlayacaksınız. Gelen banka ekstrelerini, Uluslararası Banka Hesabı Numarası (IBAN) kodlarını içeren metin (.txt) dosyaları olarak alacaksınız. Banka ekstrelerini içe aktarma işleminin bir parçası olarak, halihazırda bulunan mantığı kullanarak bu IBAN kodlarının doğru olduğunu doğrulamanız gerekir.

## <a name="prerequisites"></a>Ön Koşullar

Bu makaledeki prosedürler, **Sistem yöneticisi** veya **Elektronik raporlama geliştiricisi** rolüne atanmış kullanıcılar içindir.

Bu prosedürler herhangi bir veri kümesi kullanılarak tamamlanabilir.

Bunları tamamlamak için şu dosyayı indirmeniz ve yerel olarak kaydetmeniz gerekir: [SampleIncomingMessage.txt](https://download.microsoft.com/download/8/0/a/80adbc89-f23c-46d9-9241-e0f19125c04b/SampleIncomingMessage.txt).

Bu makalede, Litware, Inc. örnek şirketi için gerekli ER yapılandırmalarını oluşturacaksınız. Bu nedenle bu makaledeki yordamları tamamlayabilmek için önce aşağıdaki adımları tamamlamanız gerekir.

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında, **Litware, Inc.** örnek şirketine ait yapılandırma sağlayıcısının kullanılabildiğinden ve etkin olarak işaretlendiğinden emin olun. Bu yapılandırma sağlayıcısını göremiyorsanız öncelikle [Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme](er-configuration-provider-mark-it-active-2016-11.md) yordamındaki adımları tamamlamanız gerekir.

## <a name="import-a-new-er-model-configuration"></a>Yeni bir ER modeli yapılandırmasını içe aktarma

1. **Yerelleştirme yapılandırmaları** sayfasında **Yapılandırma sağlayıcıları** bölümünde **Microsoft** yapılandırma sağlayıcısı kutucuğunu seçin.
2. **Depolar**'ı seçin.
3. **Yerelleştirme depoları** sayfasında **Filtreleri göster**'i seçin.
4. Global depo kaydını seçmek için, bir **Ad** filtresi alanı ekleyin.
5. **Ad** alanına, **Genel** yazın. Ardından, **içerir** filtre işlecini seçin.
6. **Uygula**'yı seçin.
7. Seçilmiş depo için ER yapılandırmalarını görüntülemek için **[Aç](../er-download-configurations-global-repo.md#open-configurations-repository)**'a tıklayın.
8. **Yapılandırma deposu** sayfasında yapılandırma ağacında, **Ödeme modeli**'ni seçin.
9. **Sürümler** hızlı sekmesinde **İçe aktar** düğmesi mevcutsa **Evet**'i seçin.

    **İçe aktar** düğmesi etkinleştirilmemişse, ER yapılandırma **Ödeme modeli**'nin seçili sürümünü zaten içe aktarmışsınızdır.

10. **Konfigürasyon deposu** sayfasını kapatın ve sonra da **Yerelleştirme depoları** sayfasını kapatın.

## <a name="add-a-new-er-format-configuration"></a>Yeni bir ER biçim yapılandırması ekleme

TXT biçimindeki gelen banka ekstrelerini ayrıştırmak için yeni bir ER biçimi ekleyin.

1. **Yerelleştirme yapılandırmaları** sayfasında **Yapılandırmaları raporlama** kutucuğunu seçin.
2. **Yapılandırmalar** sayfasında soldaki yapılandırma ağacında, **Ödeme modeli**'ni seçin.
3. **Yapılandırma oluştur**'u seçin. 
4. Açılan iletişim kutusunda şu adımları izleyin:

    1. **Yeni** alanına, **Biçim veri modeline PaymentModel dayalı** girin.
    2. **Ad** alanına, **Banka ekstresi içe aktarma biçimi (örnek)** yazın.
    3. **Veri içe aktarmayı destekler** alanında **Evet**'i seçin.
    4. Yapılandırma oluşturmayı tamamlamak için **Yapılandırma oluştur**'u seçin.

## <a name="design-the-er-format-configuration--format"></a>ER biçimi yapılandırması tasarlama – Biçim

Harici dosyanın TXT biçimindeki beklenen yapısını gösteren bir ER biçimi tasarlayın.

1. Eklediğiniz **Banka ekstresi içe aktarma biçimi (örnek)** biçim konfigürasyonu için **Tasarımcı**'yı seçin.
2. **Biçim tasarımcısı** sayfasında, biçim yapısı ağacında **Kök ekle**'yi seçin.
3. Gösterilen iletişim kutusunda şu adımları izleyin:

    1. Ağaçta **Metin\\Sıra**'yı seçerek **Sıra** biçim bileşenini ekleyin.
    2. **Ad** alanına, **Kök** girin.
    3. **Özel karakterler** alanında **Yeni satır - Windows (CR LF)** öğesini seçin. Bu ayarı temel alarak, ayrıştırma dosyasındaki her satır ayrı bir kayıt olarak ele alınır.
    4. **Tamam**'ı seçin.

4. **Ekle**'yi seçin.
5. Gösterilen iletişim kutusunda şu adımları izleyin:

    1. Ağaçta, **Metin\\Sıra** öğesini seçin.
    2. **Ad** alanına, **Satırlar** yazın.
    3. **Çokluluk** alanında **Bir fazla**'yı seçin. Bu ayara bağlı olarak, ayrıştırma dosyasında en az bir satır sunulması beklenir.
    4. **Tamam**'ı seçin.

6. Ağaçta, **Kök\\Satırlar** öğesini ve ardından **Sıra Ekle**'yi seçin.
7. Gösterilen iletişim kutusunda şu adımları izleyin:

    1. **Ad** alanına, **Alanlar** yazın.
    2. **Çokluluk** alanında **Tam bir**'i seçin.
    3. **Tamam**'ı seçin.

8. Ağaçta, **Kök\\Satırlar\\Alanlar** öğesini ve ardından **Ekle**'yi seçin.
9. Gösterilen iletişim kutusunda şu adımları izleyin:

    1. Ağaçta **Metin\\Dize**'yi seçin.
    2. **Ad** alanına, **IBAN** yazın.
    3.. **Tamam**'ı seçin.

10. **Kaydet**'i seçin.

Yapılandırma, ayrıştırma dosyasındaki her satırı yalnızca IBAN kodunu içerecek şekilde ayarlandı.

![Biçim tasarımcısı sayfasında Banka ekstresi içe aktarma biçimi (örnek) biçim konfigürasyonu.](../media/design-expressions-app-class-er-01.png)

## <a name="design-the-er-format-configuration--mapping-to-a-data-model"></a>ER biçimi yapılandırması tasarlama – Veri modeliyle eşleme

Bir veri modelini doldurmak üzere ayrıştırma dosyasındaki bilgileri kullanan bir ER biçim eşlemesi tasarlayın.

1. **Biçim tasarımcısı** sayfasında Eylem Panosu üzerinde **Biçimi modele eşle**'yi seçin.
2. **Veri kaynağı eşleme modeli** sayfasında Eylem Panosu üzerinde **Yeni**'yi seçin.
3. **Tanım** alanında **BankToCustomerDebitCreditNotificationInitiation**'ı seçin.
4. **Ad** alanına **Veri modeline eşleme**'yi girin.
5. **Kaydet**'i seçin.
6. **Tasarımcı**’yı seçin.
7. **Model eşleme tasarımcısı** sayfasında, **Veri kaynağı türleri** ağacında, **Dynamics 365 for Operations\\Sınıf**'ı seçin.
8. **Veri kaynakları** bölümünde, IBAN kodları doğrulaması için varolan uygulama mantığını çağıran bir veri kaynağı eklemek için **Kök ekle**'yi seçin.
9. Gösterilen iletişim kutusunda şu adımları izleyin:

    1. **Ad** alanına, **Kontrol et\_kodlar** yazın.
    2. **Sınıf** alanında, **ISO7064** yazın veya seçin.
    3. **Tamam**'ı seçin.

10. **Veri kaynağı türleri** ağacında, aşağıdaki adımları izleyin:

    1. **Biçim** veri kaynağını genişletin.
    2. **biçim\\Kök: Sıra(Kök)**'ü genişletin.
    3. **biçim\\Kök: Sıra(Kök)\\Satırlar: Sıra 1..\* (Satırlar)** öğesini genişletin.
    4. **biçim\\Kök: Sıra(Kök)\\Satırlar: Sıra 1..\* (Satırlar)\\Alanlar: Sıra 1..1 (Alanlar)** öğesini genişletin.

11. **Veri modeli** ağacında, aşağıdaki adımları izleyin:

    1. Veri modelinin **Ödemeler** alanını genişletin.
    2. **Ödemeler\\Alacaklı Hesabı(CreditorAccount)** öğesini genişletin.
    3. **Ödemeler\\Alacaklı Hesabı(CreditorAccount)\\Kimlik saptama** öğesini genişletin.
    4. **Ödemeler\\Alacaklı Hesabı(CreditorAccount)\\Kimlik saptama\\IBAN** öğesini genişletin.

12. Konfigüre edilen biçimin bileşenlerini veri modeli alanlarına bağlamak için aşağıdaki adımları izleyin:

    1. **biçim\\Kök: Sıra(Kök)\\Satırlar: Sıra 1..\* (Satırlar)** öğesini seçin.
    2. **Ödemeler**'i seçin.
    3. **Bağla**'yı seçin. Bu ayarı temel alarak, ayrıştırma dosyasındaki her satır ayrı bir ödeme olarak ele alınır.
    4. **biçim\\Kök: Sıra(Kök)\\Satırlar: Sıra 1..\* (Satırlar)\\Alanlar: Sıra 1..1 (Alanlar)\\IBAN: Dize(IBAN)** öğesini seçin.
    5. **Ödemeler\\Alacaklı Hesabı(CreditorAccount)\\Kimlik saptama\\IBAN** öğesini seçin.
    6. **Bağla**'yı seçin. Bu ayara dayalı olarak, veri modelinin **IBAN** alanı, ayrıştırma dosyasındaki değerle doldurulacaktır.

    ![Model eşleme tasarımcısı sayfasındaki bileşenlerin veri modeli alanlarına biçim bağlamayı bağlama.](../media/design-expressions-app-class-er-02.png)

13. **Doğrulamalar** sekmesinde, ayrıştırmadosyasındaki geçersiz bir IBAN kodu içeren herhangi bir satır için hata iletisi gösteren bir [doğrulama](../general-electronic-reporting-formula-designer.md#Validation) kuralı eklemek için şu adımları izleyin:

    1. **Yeni**'yi seçin ve ardından **Koşulu düzenle**'yi seçin.
    2. **Formül tasarımcısı** sayfasında, **Veri kaynağı** ağacında, bu sınıfın kullanılabilir yöntemlerini görmek için **ISO7064** uygulama sınıfını temsil eden **Denetim\_kod** veri kaynağını genişletin.
    3. **Denetim\_kodlar\\verifyMOD1271\_36** öğesini seçin.
    4. **Veri kaynağını ekle**'yi seçin.
    5. **Formül** alanına şu [ifadeyi](../general-electronic-reporting-formula-designer.md#Binding) yazın: **Denetim\_codes.verifyMOD1271\_36(format.Root.Rows.Fields.IBAN)**.
    6. **Kaydet**'i seçip sayfayı kapatın.
    7. **İleti düzenle**’yi seçin.
    8. **Formül tasarımcısı** sayfasında, **Formül alanına** **CONCATENATE("Geçersiz IBAN kodu bulundu:&nbsp;", format.Root.Rows.Fields.IBAN)** girin.
    9. **Kaydet**'i seçip sayfayı kapatın.

    Bu ayarlara dayanarak, doğrulama koşulu, **ISO7064** uygulama sınıfının mevcut **verifyMOD1271\_36** yöntemini çağırarak geçersiz tüm IBAN kodları için *[YANLIŞ](../er-formula-supported-data-types-primitive.md#boolean)* değerini döndürür. IBAN kodu değerinin çalışma zamanında çağırma yönteminin bağımsız değişkeni olarak ayrıştırma metin dosyası içeri temel alınarak dinamik şekilde tanımlandığını unutmayın.

    ![Model eşleme tasarımcı sayfasında doğrulama kuralı.](../media/design-expressions-app-class-er-03.png)

14. **Kaydet**'i seçin.
15. **Model eşleme tasarımcısı** sayfasını kapatın ve sonra da **Model veri kaynağı eşleme** sayfasını kapatın.

## <a name="run-the-format-mapping"></a>Biçim eşlemeyi çalıştırma

Sınama amacıyla, daha önce yüklediğiniz SampleIncomingMessage.txt dosyasını kullanarak biçim eşlemesini çalıştırın. Oluşturulan çıktı, seçilen metin dosyasından içeri aktarılacak verileri içerir ve gerçek içe aktarma sırasında özel veri modelini doldurur.

1. **Veri kaynağı eşleme modeli** sayfasında **Çalıştır**'ı seçin.
2. **Elektronik rapor parametreleri** sayfasında, **Gözat**'ı seçin, indirdiğiniz **SampleIncomingMessage.txt** dosyasına gidin ve dosyayı seçin.
3. **Tamam**'ı seçin.
4. **Veri kaynağı eşleme modeli** sayfasında, geçersiz bir IBAN koduyla ilgili bir hata iletisi göreceksiniz.

    ![Modeli veri kaynağına eşleme sayfasında biçim eşleme çalıştırmanın sonucu.](../media/design-expressions-app-class-er-04.png)

5. Seçili dosyadan içeri aktarılan ve veri modeline taşınan verileri temsil eden XML biçimindeki çıktıyı gözden geçirin. İçe aktarılan metin dosyasının yalnızca üç satırının hatasız olarak işlendiğine dikkat edin. Satır 4'teki IBAN kodu geçerli değil ve atlanmış.

    ![XML çıktısı.](../media/design-expressions-app-class-er-05.png)

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
