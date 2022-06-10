---
title: Elektronik raporlamayı kullanarak pozitif ödeme dosyalarını ayarlama ve oluşturma
description: Bu konuda, Elektronik raporlama kullanılarak pozitif ödemenin nasıl ayarlanacağı açıklanmıştır.
author: panolte
ms.date: 03/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: bc2f17d62b429b599d5ac5f2a521819275d36b64
ms.sourcegitcommit: 2b4ee1fe05792332904396b5f495d74f2a217250
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2022
ms.locfileid: "8770261"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>Elektronik raporlamayı kullanarak pozitif ödeme dosyalarını ayarlama

Bu konuda, Elektronik raporlama kullanılarak pozitif ödemenin nasıl ayarlanacağı ve pozitif ödeme dosyalarının nasıl oluşturulacağı açıklanmıştır.

> [!NOTE] 
> **Banka pozitif ödeme dosyası oluştur** işlevini kullanmadan önce varlık listesini yenilemeniz gerekir.
> **Veri yönetimi > İçeri aktarma / Dışarı aktarma > Çerçeve parametreleri** 
> **Varlık ayarları** hızlı sekmesine gidin ve **Varlık listesini yenile**'yi seçin.


Bankaya sunulan çeklerin bir elektronik listesini oluşturmak için pozitif ödeme kurun. Bankaya bir çek sunulduğunda, banka bunu çek listesiyle karşılaştırır. Çek, çek listesindeki bir çekle uyuşuyorsa banka çeki serbest bırakır. Çek, listedeki bir çekle uyuşmuyorsa banka, çeki gözden geçirmek için tutar.

## <a name="security-for-positive-pay-files"></a>Pozitif ödeme dosyaları için güvenlik
Pozitif ödeme dosyaları, alacaklar ve çek tutarları hakkında hassas bilgiler içermektedir. Bu nedenle, banka tarafından alınana kadar dosyaların oluşturulduğu süreden itibaren uygun güvenlik önlemlerini uyguladığınızdan emin olun. Pozitif ödeme dosyaları, web tarayıcınız tarafından belirtilen konuma indirilir. Pozitif ödeme dosyaları hassas bilgiler içerebileceğinden, Microsoft Dynamics 365 Finance'te bu bilgilerin oluşturulması ve görüntülenmesinin yalnızca yetkili kullanıcılarla sınırlandırılması önemlidir. Gerekli olan ayrıcalıkları belirlerken aşağıdaki tabloyu kullanın.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Görev</th>
<th>Ayrıcalık</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Banka hesapları</strong> liste sayfasından veya <strong>Banka hesapları</strong> sayfasından pozitif ödeme dosyaları oluşturun.</td>
<td><ul>
<li><strong>Pozitif banka ödeme bilgilerini koru</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="even">
<td>Birden çok tüzel kişilik ve banka hesabı için pozitif ödeme dosyalarını <strong>Bir pozitif ödeme dosyası oluştur</strong> sayfasından oluşturun.</td>
<td><ul>
<li><strong>Pozitif banka ödeme bilgilerini koru</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Pozitif ödeme dosyalarını <strong>Pozitif ödeme dosyası özeti</strong> sayfasında görüntüleyin.</td>
<td><strong>Birden çok tüzel kişilik için banka pozitif ödeme bilgilerini görüntüle</strong> (BankPositivePayView)</td>
</tr>
<tr class="even">
<td>Bir banka pozitif ödeme dosyasını <strong>Pozitif ödeme dosyası özeti</strong> sayfasında onaylayın.</td>
<td><strong>Pozitif ödeme dosyasını onayla</strong> (BankPositivePayConfirm)</td>
</tr>
<tr class="odd">
<td>Bir banka pozitif ödeme dosyasını <strong>Pozitif ödeme dosyası özeti</strong> sayfasında geri çağırın.</td>
<td><strong>Pozitif ödeme dosyasını geri çağır</strong> (BankPositivePayRecall)</td>
</tr>
</tbody>
</table>

## <a name="set-up-the-electronic-reporting-configuration"></a>Elektronik raporlama yapılandırmasını ayarlama

1. Sırasıyla **Çalışma alanları \> Elektronik raporlama**'ya gidin.
2. **Microsoft** yapılandırma sağlayıcısı kutucuğunda **Depolar**'ı seçin.
3. **Genel**'i seçin ve **Aç**'ı seçin.
4. Depoya bir bağlantı kurulması gerekiyorsa, iletişim kutusundaki mavi bağlantıyı seçin.
5. Yapılandırma listesinde, **Pozitif ödeme modeli \> Pozitif ödeme biçimi**'ni bulup seçin.
6. **Sürümler** hızlı sekmesinde, en son sürümü ve sonra **İçe aktar**'ı seçin.

## <a name="set-up-a-positive-pay-format"></a>Bir pozitif ödeme biçimi kurma

1. **Nakit ve banka yönetimi \> Kurulum \> Pozitif ödeme biçimleri** seçeneğine gidin.
2. **Yeni**'yi seçin.
3. **Ödeme biçimi** ve **Açıklama** alanlarını ayarlayın.
4. **Genel elektronik dışa aktarma biçimi** onay kutusunu seçin.
5. **Dışa aktarma biçimi yapılandırma** alanını **Pozitif ödeme biçimi**'ne ayarlayın.

## <a name="assign-a-positive-pay-format-to-a-bank-account"></a>Pozitif ödeme biçimini bir banka hesabına atama
Pozitif ödeme bilgisi oluşturmak istediğiniz her bir banka hesabı için, önceki bölümde tanımladığınız pozitif ödeme biçimini atamanız gerekir. Banka hesaplarını sayfasında, banka hesabına karşılık gelen pozitif ödeme biçimini seçin. **Pozitif ödeme başlangıç tarihi** alanında, pozitif ödeme dosyaları oluşturmak için başlangıç tarihini girin. 

>[!Important]
> **Pozitif ödeme başlangıç tarihi** alanına bir tarih girin. Boş bırakılırsa, oluşturulan ilk pozitif ödeme dosyası bu banka hesabı için oluşturulan tüm çekleri içerir.

1. **Nakit ve banka yönetimi \> Banka hesapları \> Banka hesapları** öğesine gidin.
2. Banka hesabını açın.
3. **Genel** hızlı sekmesinde, **Pozitif ödeme biçimi** alanını daha önce oluşturulan biçime ayarlayın.
4. **Pozitif ödeme başlangıç tarihi** alanını mevcut tarih olarak ayarlayın.

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>Pozitif ödeme dosyaları için bir numara serisi atama
Her bir pozitif ödeme dosyası mutlaka kendine özel bir numaraya sahip olmalıdır. **Nakit ve banka yönetimi parametreleri** sayfasında, **Numara serileri** sekmesinde pozitif ödeme dosyaları için numara serisi oluşturun.

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>Bir tekli banka hesabı için bir pozitif ödeme dosyası oluşturma
Tek bir tüzel kişilik ve tek bir banka hesabı için bir pozitif ödeme dosyası oluşturabilirsiniz. Pozitif ödeme dosyalarının aynı anda birden fazla tüzel kişilik ve banka hesabı için nasıl oluşturulacağı hakkında daha fazla bilgi için bir sonraki bölüme bakın. Tek bir tüzel kişilik ve tek bir banka hesabı için bir pozitif ödeme dosyası oluşturmak **Banka hesapları** sayfasından **Bir pozitif ödeme dosyası oluştur** iletişim kutusunu açın. **Sonlandırma tarihi** alanında, pozitif ödeme dosyasına eklenecek son çek tarihini girin. Bu kontrol tarihinin sonuna kadar bir pozitif ödeme dosyasına dahil edilmemiş tüm çekler dosyaya dahil edilir.

1. **Nakit ve banka yönetimi \> Banka Hesapları \> Banka Hesapları** öğesine gidin.
2. Pozitif ödemenin ayarlandığı bir banka hesabını açın.
3. **Ödemeleri yönet \> Pozitif ödeme \> Pozitif ödeme dosyası**'nı seçin.
4. **Kesme tarihi** alanını ayarlayın. Bu tarihten önce oluşturulan çekler dahil edilir.

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>Birden fazla banka hesabı için bir pozitif ödeme dosyası oluşturma
Birden fazla banka hesabı için bir pozitif ödeme dosyası oluşturmak üzere **Pozitif ödeme dosyası** periyodik görevini kullanın. Dosya için pozitif ödeme biçimini seçin ve dosyanın tüm tüzel kişilikler için mi, yoksa seçilen bir tüzel kişilik için mi oluşturulacağını belirleyin. Ayrıca, belirtilen pozitif ödeme biçimini kullanan tüm banka hesapları veya seçilen bir banka hesabı için pozitif ödeme dosyası oluşturabilirsiniz. **Sonlandırma tarihi** alanında, pozitif ödeme dosyasına eklenecek son çek tarihini girin. Bu kontrol tarihinin sonuna kadar bir pozitif ödeme dosyasına dahil edilmemiş tüm çekler dosyaya dahil edilir.

## <a name="view-the-results-of-positive-pay-file-generation"></a>Pozitif ödeme dosyası oluşturma sonuçlarını görüntüleme
Pozitif ödeme dosyası oluşturulduktan sonra sonuçları **Pozitif ödeme dosyası özeti** sayfasında görüntüleyebilirsiniz. Her bir çekin ayrıntılarını görüntülemek için **Pozitif ödeme dosyası ayrıntıları** sayfasına gidin.

## <a name="confirm-a-positive-pay-file"></a>Bir pozitif ödeme dosyasını onaylama
Bir pozitif ödeme dosyasında listelenen çekler ödendikten sonra bankanızdan bir onay numarası alırsınız. Pozitif ödeme dosyasını onaylayabilirsiniz. **Pozitif ödeme dosyası özeti** sayfasında, durumu **Oluşturuldu** olan bir pozitif ödeme dosyası seçin ve ardından **Onay gir** eylemini seçin. Bir pozitif ödeme dosyasını onayladığınızda, bankadan aldığınız onay numarası kaydedilir.

## <a name="recall-a-positive-pay-file"></a>Bir pozitif ödeme dosyasını geri çağırma
Bir pozitif ödeme dosyasını değiştirmeniz gerekiyorsa, bunu geri çağırabilirsiniz. **Pozitif ödeme dosyası özeti** sayfasında, durumu **Oluşturuldu** olan bir pozitif ödeme dosyası seçin ve ardından **Geri çağır** eylemini seçin. Pozitif ödeme dosyasındaki her bir çek için, çekin bir pozitif ödeme dosyasına dahil edilip edilmeyeceğini gösteren alan sıfırlanır. Geri çağrılan çeki içeren, yeni bir pozitif ödeme dosyası oluşturabilirsiniz.


Elde edilen XML dosyası indirilir.
