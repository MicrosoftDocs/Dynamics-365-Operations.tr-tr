---
title: Basit bir ER dışa aktarma biçimini, bir Excel raporu oluşturmak için ayarlayın ve çağırın
description: Bu makalede, elektronik iletilerin nasıl ayarlanacağını ve kullanılacağını gösteren bir örnek yer almaktadır.
author: liza-golub
ms.date: 07/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 9894aabde854189e6fc1b6bb62051747f190e3ec
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904600"
---
# <a name="set-up-and-run-processing-to-call-a-simple-exporting-er-format-to-generate-an-excel-report"></a>Basit bir ER dışa aktarma biçimini, bir Excel raporu oluşturmak için ayarlayın ve çağırın

[!include [banner](../includes/banner.md)]

ER biçiminizi oluşturduktan, veri kaynaklarına eşleştirdikten ve tamamladıktan sonra, bunu **Elektronik raporlama** çalışma alanından çalıştırabilirsiniz. Rapor oluşturulduktan sonra yerel olarak kaydedebilirsiniz.

Raporlama işleminin aşağıdaki yönlerini kontrol etmek için, elektronik ileti işlemeyi ayarlayın:

- Raporu kimin oluşturduğuna dair günlük bilgisi.
- Raporun ne zaman oluşturulduğunda dair günlük bilgisi.
- Önceki dönemler için oluşturulmuş raporları kaydet.

Aşağıdaki örnek, Microsoft Excel için bir dışa aktarma ER biçimine dayanan bir rapor oluşturmak için elektronik mesajlaşmayı nasıl kurabileceğinize dair bir örnek gösterir. Bu örneği takip etmek istiyorsanız, Excel için dışarı aktarma ER biçimini halihazırda oluşturulmuş, veri kaynaklarına eşleştirilmiş ve tamamlanmış olması gerekir. Ek olarak, bir numara serisinin elektronik iletiler için zaten ayarlanmış olması gerekir.

İşleme kurduğunuzda, ilk önce ayarlanacak işleme eylemlerini ve durumlarını tanımlamanız yararlıdır. Aşağıdaki çizim, bu örnekte işlemenin nasıl göründüğünü göstermektedir.

![İşleme düzeni](media/processing-scheme.png)

## <a name="create-message-statuses"></a>Mesaj durumları oluşturmak

1. **Vergi** \> **Kurulum** \> **Elektronik iletiler** \> **İleti durumları**'na gidin.
2. Aşağıdaki mesaj durumlarını oluşturun:

    - Yeni
    - Hazırlandı
    - Oluşturuldu

    ![İleti durumları](media/message-statuses.png)

3. **Yeni** durum satırında, **Silmeye izin ver** onay kutusunu seçerek kullanıcıların bu duruma sahip mesajları silmesine izin verin.

## <a name="create-additional-fields"></a>Ek alanlar oluştur

1. **Vergi** \> **Kurulum** \> **Elektronik iletiler** \> **Ek alanlar**'a gidin.
2. Başka bir alanı ve değerlerini ekleyin.
3. **Kullanıcı düzenlemesi** seçeneğini **Evet** olarak ayarlayarak kullanıcıların alanı düzenlemesine izin verin.

![Ek alanlar](media/additional-fields.png)

## <a name="create-message-processing-actions"></a>Mesaj işleme eylemleri oluşturun

Bu örnek için, aşağıdaki ileti işleme eylemlerini oluşturacaksınız:

- **İleti oluştur**
- **Hazırlanmışa Güncelleştir**
- **Rapor oluştur**
- **Başlangıç durumuna güncelleştir** (isteğe bağlı)

Eylemleri oluşturmak için aşağıdaki adımları izleyin.

1. **Vergi** \> **Kurulum** \> **Elektronik mesajlaşma** \> **Mesaj işleme eylemleri**'ne gidin.
2. **Mesaj oluştur** olarak adlandırılmış bir eylem oluşturun. **Genel** FastTab'i üzerinde, **Eylem türü** alanında **Mesaj oluştur**'u seçin.
3. **Hazırlanmışa Güncelleştir** olarak adlandırılmış olan bir eylem oluşturun ve aşağıdaki alanları ayarlayın:

    - **Genel** FastTab'i üzerinde, **Eylem türü** alanında **Mesaj düzeyi kullanıcı işleme**'yi seçin.
    - **Başlangıç durumlar** FastTab'inde, **Mesaj durumu** alanında, **Yeni**'yi seçin.
    - **Sonuç durumları** FastTab'inde, **Mesaj durumu** alanında, **Hazırlanmış**'ı seçin. **Yanıt türü** alanında, **Başarıyla yürütüldü** girin.

4. **Rapor oluştur** olarak adlandırılmış olan bir eylem oluşturun ve aşağıdaki alanları ayarlayın:

    - **Genel** FastTab'i üzerinde, **Eylem türü** alanında **Elektronik raporlama dışa aktarma**'yı seçin. **Biçim eşleştirme** alanında, ER biçimi dışa aktarmayı seçin. Seçenekler **Excel**, **XML**, **JSON**, **Metin** ve **Diğer**'dir.
    - **Başlangıç durumları** FastTab'inde, **Mesaj durumu** alanında, **Hazırlanmış**'ı seçin.
    - **Sonuç durumları** FastTab'inde, **Mesaj durumu** alanında, **Oluşturuldu**'yu seçin. **Yanıt türü** alanında, **Başarıyla yürütüldü** girin.

    ![Rapor eylemi oluştur](media/generate-report-action.png)

5. İsteğe bağlı: Kullanıcıların bir raporu birden fazla kez yeniden oluşturmasına izin vermek için **Başlangıç durumuna güncelleştir** adlı bir eylem oluşturun ve aşağıdaki alanları ayarların:

    - **Genel** FastTab'i üzerinde, **Eylem türü** alanında **Mesaj düzeyi kullanıcı işleme**'yi seçin.
    - **Başlangıç durumları** FastTab'inde, **Mesaj durumu** alanında, **Oluşturuldu**'yu seçin.
    - **Sonuç durumlar** hızlı sekmesinde, iki ileti durumunun her biri için ayrı bir satır ekleyin (**Hazırlandı** ve **Yeni**). Her iki satır için, **Yanıt türü** alanını **Başarıyla yürütüldü** olarak ayarlayın.

## <a name="electronic-message-processing"></a>Elektronik ileti işleme

Bu örnekte, tüm eylemler ayrı yürütülebilecek şekilde ayarlanmış olmalıdır. Varsayım, her kullanıcının her eylemi başlatacağıdır.

1. **Vergi** \> **Kurulum** \> **Elektronik iletiler** \> **Elektronik ileti işleme**'ye gidin.
2. İşlemeni için bir kayıt girin, tüm önceden tanımlanmış eylemleri ekleyin ve bir ek alan ekleyin.
3. İsteğe bağlı: **Güvenlik rolleri** FastTab'inde, belirli raporlamalara erişimi kısıtlamak için güvenlik rollerini tanımlayın.
4. **Vergi** \> **Sorgular ve raporlar** \> **Elektronik iletiler** \> **Elektronik iletiler**'e gidin.
5. Bir mesaj oluşturmak için **Yeni**'yi seçin. Bu noktada, tarihler ve bir açıklama ekleyebilirsiniz. Ayrıca, ihtiyaç duyarsanız ek alanların değerlerini de güncelleştirebilirsiniz.

    ![Bir elektronik ileti oluşturma](media/create-electronic-message.png)

    **Eylem günlüğü** FastTab'i üzerindeki kılavuz, mesaj üzerinde gerçekleştirilmiş olan tüm eylemlerin bir kaydı ile otomatik olarak doldurulur.

    Şimdi ileti durumunu silebilir veya güncelleştirebilirsiniz. 

6. Mesaj durumunu güncelleştirmek için **Durumu güncelleştir**'i seçin. **Yeni durum** alanında, **Hazırlanmış**'ı seçin ve sonra **Tamam**'ı seçin.

    ![İleti durumunu güncelleştirme](media/update-status.png)

    İleti durumu **Hazırlandı** olarak güncelleştirilir.

7. **Rapor Oluştur** öğesini seçerek raporu oluşturun.

    Rapor oluşturulur ve mesaj durumu ve eylem günlüğü güncelleştirilir.

8. Oluşturulan raporu görüntülemek için sayfanın sağ üst köşesinde bulunan **Ek** düğmesini seçin (ataş simgesi).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
