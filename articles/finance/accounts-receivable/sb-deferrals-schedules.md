---
title: Gelir ve gider ertelemelerinde erteleme planları
description: Bu konuda, gelir ve gider ertelemelerindeki erteleme planları açıklanmaktadır.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 9135ac733496a0c5d79669c35972c273c209f81d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685991"
---
# <a name="deferral-schedules"></a>Erteleme planları

Erteleme planları bir hareket deftere nakledildikten sonra oluşturulur.

Erteleme planıyla ilgili ayrıntıları gözden geçirmek için, **Tüm erteleme planları** veya **Etkin erteleme planları** sayfasını kullanabilirsiniz. Gösterilen bilgiler erteleme planı türüne (eşit paylı veya olay tabanlı) ve hareket türüne bağlıdır. Erteleme planı satırlarını ve erteleme planı için toplam tutarları içerir. Erteleme planını düzenlemek için sayfayı kullanabilirsiniz.

## <a name="recognize-revenue"></a>Geliri kabul etme

> [!NOTE]
> - Bir erteleme planının gelirini kabul etmek için adım 1'den başlayın.
> - Birden fazla planın gelirini kabul etmek için adım 2'den başlayın.

1. **Tüm erteleme planları** sayfasında, **Plan satırları** kılavuzunda, kabul etmek istediğiniz satırları ve ardından **Kabul et**'i seçin.
2. **Kabul işleme** sayfasında, **Kabul eylemi** alanını **Kabul günlüğü oluştur**'a ayarlayın.
3. **Kesme tarihi** alanında kesme tarihini seçin. İşlem yalnızca, bitiş tarihinin seçili kesme tarihi ile aynı veya bundan daha eski olduğu satırları dahil eder.
4. **Filtre**'yi seçin ve veri filtreleri ekleyin; böylece liste yalnızca istediğiniz kayıt aralığını gösterir.
5. Satırları görüntülemek için **Önizlemeyi görüntüle**'yi seçin.
6. Satır listesinde, işlemek istemediğiniz satırları seçin ve **Kaldır**'ı seçin.
7. Kabul günlüğü girişini özetlemek isteyip istemediğinizi seçin.
8. **Hareket tarihi** bölümünde, hareketi işlemek için hareket tarihini belirli bir tarihle geçersiz kılabilirsiniz. Kapalı dönemler için hareket tarihi belirtilebilir.
9. İşlemeyi bir toplu işin parçası olarak yapmak için **Toplu iş**'i seçin. **Toplu işleme** iletişim kutusunda toplu işle ilgili parametreleri ayarlayın ve sonra da **Kabul işleme** sayfasına dönmek için **Tamam**'ı seçin. Gelir kabulü, daha sonra toplu iş işlenirken işlenecektir.
10. **İşlem**'i seçin. Hareketi bir toplu işe eklemediyseniz, tüm satırlar derhal işlenir. Aksi takdirde, satırlar toplu iş işlenirken işlenir.

## <a name="modify-a-schedule"></a>Bir planı değiştirme

Erteleme planını değiştirmek için bu adımları izleyin.

1. **Tüm erteleme planları** sayfasında erteleme planını seçin ve sonra **Muhasebe \> Planı değiştir**'i seçin.
2. **Planı değiştir** sayfasında, değiştirmek istediğiniz seçenekleri düzenleyin. Erteleme planına bağlı olarak, tüm seçenekleri düzenleyemezsiniz.
3. Erteleme planında yapılan değişiklikleri gözden geçirmek için **Önizleme**'yi seçin.
4. **Tamam**'ı seçin.

### <a name="straight-line-deferral-schedules"></a>Eşit paylı erteleme planları

Erteleme planının kabul edilen veya harici olarak deftere nakledilen satırları yoksa, başlangıç tarihi dahil olmak üzere tüm erteleme planını değiştirebilirsiniz.

Erteleme planının herhangi bir kabul edilen veya harici deftere nakledilmiş satırı varsa ve erteleme planını değiştirirseniz, erteleme planının ortaya çıkan davranışı, yeniden hesaplama tarihine ve kabul edilen satırların erteleme bitiş tarihine bağlıdır. Varsayılan olarak, kabul edilmeyen ilk dönem, erteleme bitiş tarihini belirler.

Kabul tarihini kullanmak için, **Plan başlangıcı** alanında aşağıdaki değerlerden birini seçin: 
- **Yakalama** – Tüm kabul edilen satırlar hesaplandıktan sonraki tutar.
- **Ters işlem** – Yeniden hesaplama tarihinden sonraki herhangi bir satır, belirtilen günlük adı ve deftere nakil tarihi kullanılarak tersine çevrilir. Yeniden hesaplama tarihinden sonraki tutar yeniden hesaplanır.

Bir şablon kullanılırsa, atlanan dönemler dikkate alınmaz ve şablon yalnızca bitiş tarihini hesaplamak için kullanılır.

### <a name="event-based-deferral-schedules"></a>Olay tabanlı erteleme planları

Olay tabanlı erteleme planı için, kabul edilmeyen tüm satırları değiştirebilirsiniz.

Erteleme planının kabul edilen veya harici olarak deftere nakledilen satırı varsa, erteleme planının şablonunu ve tahsisat türünü değiştiremezsiniz. Varolan bir erteleme planını değiştirdiğinizde, **Her birim için ayrı olaylar oluştur** değerini değiştiremezsiniz.

Bir satır kabul edilirse veya harici olarak deftere nakledilirse **Kabul edildi** onay kutusu seçilir.

## <a name="modify-a-deferral-or-recognition-account"></a>Erteleme veya kabul hesabını değiştirme

Erteleme hesabının erteleme veya kabul hesabını değiştirmek için aşağıdaki adımları izleyin.

1. **Tüm erteleme planları** sayfasında erteleme planını seçin ve sonra **Muhasebe \> Hesabı değiştir**'i seçin.
2. **Hesabı Değiştir** sayfasında, değiştirmek istediğiniz hesabı (erteleme, kısa vadeli veya kabul) seçin.
3. **Yeni hesap** alanında, yeni hesabı seçin.
4. Hesapta yapılacak değişikliklerin düzeltme günlüğü girişleri oluşturup oluşturmayacağını seçin.
5. Seçeneği önceki adımda **Evet** olarak ayarlarsanız, **Günlük adı** alanında günlük adını seçin ve hareket tarihini **Hareket tarihi** alanında belirtin.
6. **Tamam**'ı seçin.

## <a name="put-a-deferral-schedule-on-hold"></a>Erteleme planını beklemeye alma

Erteleme planını beklemeye almak için bu adımları izleyin.

1. **Tüm erteleme planları** sayfasında erteleme planını seçin ve sonra **Bekletme \> Bekletme uygula**'yı seçin.
2. **Bekletme uygula** sayfasında, bakiyeyi erteleme hesabından mı yoksa bekletme hesabından mı aktarmak istediğinizi seçin.
3. Bakiyeyi aktarmayı seçtiyseniz **Günlük adı** alanında günlük adını seçin, **Beklemedeki hesap** alanında bekleme hesabını seçin ve hareket tarihini **Hareket tarihi** alanında belirtin.
4. **Tamam**'ı seçin.

## <a name="remove-a-hold-from-a-deferral-schedule"></a>Erteleme planındaki bekletmeyi kaldırma

Bir erteleme planındaki bekletmeyi kaldırmak için aşağıdaki adımları izleyin.

1. **Tüm erteleme planları** listesinde erteleme planını seçin ve sonra **Bekletme \> Bekletmeyi kaldır**'ı seçin.
2. **Günlük adı** alanında, günlük adını seçin.
3. **Hareket tarihi** alanında hareket tarihini belirtin.
4. **Tamam**'ı seçin.

## <a name="cancel-unrecognized-amounts"></a>Tanınmayan tutarları iptal et

> [!NOTE]
> Önceden kabul edilmiş veya harici olarak deftere nakledilmiş olan satırlar bu işlemden çıkarılır.

Erteleme planındaki kabul edilmeyen tutarları iptal etmek için bu adımları izleyin.

1. **Tüm erteleme planları** sayfasında erteleme planını seçin ve sonra **İptal et \> Kabul edilmeyen tutarlar**'ı seçin.
2. **Kabul edilmeyen tutarı iptal et** sayfasında, iptal girişleri oluşturmak isteyip istemediğinizi seçin.
3. İptal girişleri oluşturmayı seçtiyseniz **Günlük adı** alanında günlük adını seçin, **İptal hesabı** alanında iptal hesabını seçin ve hareket tarihini **Hareket tarihi** alanında belirtin.
4. **Tamam**'ı seçin.

## <a name="cancel-a-completed-schedule"></a>Tamamlanan bir planı iptal etme

Kabul edilen veya harici olarak deftere nakledilen tüm tutarları geri almak için **Tüm erteleme planları** sayfasını kullanın ve daha fazla kabul işlemini önlemek için erteleme planını iptal edin.

Tüm erteleme planını iptal etmek için bu adımları izleyin.

1. **Tüm erteleme planları** sayfasında erteleme planını seçin ve sonra **İptal et \> Planı tamamla**'yı seçin.
2. **Tamamlanan planı iptal et** sayfasında, iptal girişleri oluşturmak isteyip istemediğinizi seçin.
3. İptal girişleri oluşturmayı seçtiyseniz **Günlük adı** alanında günlük adını seçin, **İptal hesabı** alanında hesabı seçin ve hareket tarihini **Hareket tarihi** alanında belirtin.
4. **Tamam**'ı seçin.

## <a name="reverse-transactions"></a>Hareketleri tersine çevir

> [!NOTE]
> - Bir erteleme planının gelir kabulünü tersine çevirmek için adım 1'den başlayın.
> - Birden fazla erteleme planının gelir kabulünü tersine çevirmek için adım 2'den başlayın.

1. **Tüm erteleme planları** sayfasında, **Plan satırları** kılavuzunda, kabul etmek istemediğiniz satırları ve ardından **Tersine çevir**'i seçin.
2. **Kabul işleme** sayfasında, **Kabul eylemi** alanını **Kabul günlüğünü tersine çevir**'e ayarlayın.
3. **Kesme tarihi** alanında kesme tarihini seçin. İşlem yalnızca, bitiş tarihinin belirtilen kesme tarihi ile aynı veya bundan daha eski olduğu satırları dahil eder.
4. **Filtre**'yi seçin ve veri filtreleri ekleyin; böylece liste yalnızca istediğiniz kayıt aralığını gösterir.
5. Satırları görüntülemek için **Önizlemeyi görüntüle**'yi seçin.
6. Satır listesinde, işlemek istemediğiniz satırları seçin ve **Kaldır**'ı seçin.
7. **Ad** ve **Açıklama** alanları, varsayılan günlük adı ve açıklaması ile otomatik olarak güncelleştirilir. Değerleri istediğiniz gibi değiştirebilirsiniz. Kabul günlüğü girişini özetlemek isteyip istemediğinizi de seçebilirsiniz.
8. **Hareket tarihi** bölümünde, hareketi işlemek için hareket tarihini belirli bir tarihle geçersiz kılabilirsiniz. Kapalı dönemler için hareket tarihi belirtilebilir.
9. İşlemeyi bir toplu işin parçası olarak yapmak için **Toplu iş**'i seçin. **Toplu işleme** iletişim kutusunda toplu işle ilgili parametreleri ayarlayın ve sonra da **Kabul işleme** sayfasına dönmek için **Tamam**'ı seçin. Gelir kabulünü tersine çevirme, daha sonra toplu iş işlenirken işlenecektir.
10. **Tamam**'ı seçin. Hareketi bir toplu işe eklemediyseniz, tüm satırlar derhal işlenir. Aksi takdirde, satırlar toplu iş işlenirken işlenir.

## <a name="apply-or-unapply-a-credit-note"></a>Alacak dekontu uygulama veya uygulanmasını kaldırma

Bir alacak dekontu uygulamak için aşağıdaki adımları izleyin.

> [!NOTE]
> **Satış siparişi hareket ertelemesi** sayfasından bir alacak dekontu oluşturduğunuzda ve **Varolan planı düzelt** seçeneğini **Evet** olarak ayarladığınızda, alacak dekontu deftere nakledildiğinde alacak dekontu otomatik olarak plana uygulanır.

1. **Tüm erteleme planları** sayfasında erteleme planını seçin.
2. **Alacak düzeltmeleri** listesinde bir satır seçin ve **Uygula**'yı seçin.
3. **Alacak dekontu uygula (ertelemeler)** sayfasında, **Yeniden hesaplama tarihi** alanında yeniden hesaplama tarihini ve **Bitiş tarihi** alanında bitiş tarihini belirtin.
4. **Üst bilgi** listesinde, alacak dekontlarına sahip **Satış siparişi**'ni seçin.
5. **Satırlar** listesinde, satırı seçin.
6. **Tamam**'ı seçin.
7. **Evet**'i seçin.

> [!NOTE]
> Farklı faturalardaki birkaç ayrı öğeye alacak dekontu uygulamak için bu adımları tekrarlamak zorundasınız.

Bir alacak dekontunun uygulanmasını kaldırmak için aşağıdaki adımları izleyin.

1. **Tüm erteleme planları** sayfasında erteleme planını seçin.
2. **Alacak düzeltmeleri** listesinde faturayı seçin ve **Uygulamayı kaldır**'ı seçin.
3. **Evet**'i seçin.

## <a name="fields"></a>Alanlar

**Tüm erteleme planları** sayfası, aşağıdaki alanları içerir.

| Alanlar | Açıklama |
|--------|-------------|
| **Üst bilgi** | |
| **Plan** | |
| Tahsisat türü | Tahsisat türü, olay tabanlı erteleme için: **Yüzde** veya **Tutar**. |
| Yeniden sınıflandırma tarihi | <p>Erteleme planı için kısa vadeli yeniden sınıflandırmanın işlendiği en son tarih. Bu tarih, erteleme planı için **Olay kısa vadeli yeniden sınıflandırması** her kullanıldığında güncelleştirilir.</p>Bu alan yalnızca, kısa vadeli erteleme yöntemi olarak dinamik dönemleri veya sabit yıl kullanıldığında kullanılabilir. |
| **Hesap** | |
| Erteleme hesabı | Erteleme tutarı için kullanılan hesap. |
| Kabul hesabı | Kabul tutarı için kullanılan hesap. |
| Kabul türü | Kabul türü. |
| Dağıtım türü | Dağıtım türü. |
| **Hareket** | |
| Oluşturma kaynağı | Hareketin oluşturulduğu kaynak. |
| Hareket türü | Hareket türü. |
| Satış siparişi | Satış siparişi numarası. |
| Fatura | Fatura numarası. |
| Öğe | Madde numarası. |
| **Fatura planı** | |
| Fatura planı numarası | İlgili faturalama planının numarası. |
| Faturalama satırı durumu | İlgili faturalama planı satır maddesinin durumu. |
| Harici referanslar | Faturalama planından gelen harici referanslar hakkında bilgi: **Harici** ve **Satır numarası**. |
| Toplamlar | <p>Erteleme planı için tutar toplamları:</p><ul><li>**Uzun vadeli** – Uzun dönemli ertelenen tutarların toplamı. Bu değer yalnızca, **Gelir ve gider erteleme parametreleri** sayfasındaki **Kısa vadeli erteleme yöntemi** alanı **Yok** olarak ayarlandıysa veya kısa dönem tutarı 0'dan (sıfır) büyükse kullanılabilir.</li><li>**Kısa vadeli** – Kısa dönemli ertelenen tutarların toplamı. Bu değer yalnızca, **Gelir ve gider erteleme parametreleri** sayfasındaki **Kısa vadeli erteleme yöntemi** alanı **Yok** olarak ayarlandıysa veya kısa dönem tutarı 0'dan (sıfır) büyükse kullanılabilir.</li><li>**Kabul edilmedi** – Tüm satırlar için kabul edilmeyen tutarların toplamı.</li><li>**Koçan oluşturuldu** – Tüm satırlar için harici olarak deftere nakledilen tutarların toplamı.</li><li>**Kabul edildi** – Tüm satırlar için kabul edilen tutarların toplamı.</li><li>**Harici olarak deftere nakledildi ve kabul edildi** – Tüm satırlar için harici olarak deftere nakledilen ve kabul edilen tutarların toplamı.</li><li>**Toplam tutar** – Tüm satırlar için tutarların toplamı.</li></ul> |
| **Plan satırları** | |
| Satır | Satır sıra numarası. |
| Erteleme başlangıç tarihi | Erteleme planının başlangıç tarihi. |
| Erteleme bitiş tarihi | Erteleme planının bitiş tarihi. |
| Tutar | Erteleme tutarı. |
| Harici olarak deftere nakledildi | Satırın harici olarak deftere nakledilip nakledilmediğini gösteren bir değer. |
| Kabul Edildi | Satırın kabul edilip edilmediğini gösteren bir değer. |
| Günlük toplu iş numarası | Tutarın kabul edildiği toplu iş numarası. |
| Olay Açıklaması | Olayın açıklaması. Bu alan yalnızca olay tabanlı erteleme planları için kullanılabilir. |
| **Alacak düzeltmeleri** | |
| Fatura | <p>Fatura numarası.</p><p>Değer, erteleme planına zaten uygulanmış olan alacak dekontu düzeltmesinin faturasını belirtir.</p> |
| Uygulanan tutar | Erteleme planına zaten uygulanmış olan alacak düzeltme tutarı. |
| Uygulama tarihi | Alacak düzeltmesinin uygulanma tarihi. |
| **Düzeltme** | Düzeltme değerleri yalnızca erteleme planı için bir alacak faturası işlendiyse görüntülenir. Herhangi bir alacak dekontu işlenmediği takdirde bu değerler gizlidir. |
| Ayarlama tutarı | Toplam düzeltme tutarı, *Orijinal tutar* – *Plan tutarı* olarak hesaplanır. |
| Orijinal bitiş tarihi | Erteleme planının orijinal bitiş tarihi. |
| Orijinal plan tutarı | Orijinal erteleme planının toplam tutarı. |
