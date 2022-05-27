---
title: Personel eylemleriyle ilgili SSS
description: Bu konu, kuruluşununuz personel eylemleri kullanıyorsa sahip olabileceğiniz sorulara yanıtlar içerir.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 0782f686c9c91d434214724e2f621225a9e268b3
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692156"
---
# <a name="personnel-actions-faq"></a>Personel eylemleriyle ilgili SSS


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konu, kuruluşununuz personel eylemleri kullanıyorsa sahip olabileceğiniz sorulara yanıtlar içerir. Personel eylemleri, personelle ilgili çeşitli görevleri gerçekleştirdiğinizde tamamlamanız gereken ek adımlardır. 

Personel eylemleri gerektirebilecek görev örnekleri şunlardır:
 - Yeni pozisyonlar oluşturduğunuzda. 
 - Varolan pozisyon değerlerini değiştirin. 
 - Yeni çalışanlar işe alın. 
 - Çalışanları transfer edin. 
 - Çalışan tazminatını değiştirin. 
 - Pozisyon atamalarını değiştirin. 
 - Çalışanları işten çıkarın.

> [!NOTE]
> Personel eylemleri yalnızca **Personel eylemlerini etkinleştir** ve **Konum eylemlerini etkinleştir** alanları **Evet** olarak **Personel eylemleri** sekmesinde, **İnsan kaynakları paylaşılan parametreleri** sayfasında ayarlanmışsa kullanılabilir. 

## <a name="how-can-i-tell-if-my-organization-requires-personnel-actions"></a>Kuruluşumun personel eylemlerine ihtiyaç duyup duymadığını nasıl anlarım?
Personel eylemleri, yeni bir pozisyon oluşturduğunuzda, mevcut pozisyonları değiştirdiğinizde, yeni çalışanları işe aldığınızda, çalışanları transfer ettiğinizde, çalışan ücretini değiştirdiğinizde, pozisyon atamalarını değiştirdiğinizde, çalışanların işine son verdiğinizde veya çalışanlar için izin girdiğinizde bir personel eylemi seçmeniz isteniyorsa gereklidir. 

## <a name="what-is-the-difference-between-a-position-action-and-a-worker-action"></a>Bir pozisyon eylemi ve çalışan eylemi arasındaki fark nedir?
İki türde personel eylemi vardır:

- **Pozisyon** eylemi – Bir pozisyon eylemi mevcut pozisyonlar veya yeni pozisyonlar üzerinde gerçekleştirilir. Örneğin, bir pozisyon eylemi, mevcut bir pozisyondaki bir değeri değiştirdiğinizde veya yeni bir dönemsel pozisyon oluşturduğunuzda gerekli olabilir. 

- **Çalışan** eylemi – Bir çalışan eylemi mevcut personel veya yeni personel üzerinde gerçekleştirilir. Örneğin, yeni bir personel işe alındığında veya mevcut bir personel terfi ettirildiğinde bir çalışan eylemi gerekebilir. 

## <a name="what-do-the-statuses-of-the-personnel-actions-mean"></a>Personel eylemlerinin durumları ne anlama geliyor?
Personel eylemleri aşağıdaki durumlara sahip olabilir:

- **Taslak** – İş akışı kullanılıyorsa, eylem henüz gönderilmemiştir. İş akışı kullanılmıyorsa, eylem tamamlanmamıştır.
- **Gözden geçiriliyor** – Personel eylemi iş akışı gönderildi ancak iş akışı tamamlanmadı.
- **Onaylı bekleme** – İş akışı tamamlandı ancak değişiklikler halen sürüyor. **İptal edildi** – İş akışı iptal edildi veya personel eylemi geri çekildi. **Reddedildi** – Eylem talebi, onaylayıcı tarafından reddedildi.
- **Eylem işleniyor** – Eylem talebi onaylandı ve değişiklikler işleniyor.
- **İş akışı tamamlandı**  – İş akışı tamamlandı ve değişiklikler işlendi. **Başarısız oldu** – Bilgi günce olmadığı için iş akışı başarısız oldu. En son bilgileri görüntülemek ve devam etmek için **Yeniden etkinleştir**'i tıklatın.
- **Tamamlandı** – Pozisyon başarıyla oluşturuldu veya değiştirildi veya personel başarıyla işe alındı, transfer edildi veya işine son verildi ya da ücreti değiştirildi. **Hata** – Bilginin güncel olmaması dışında bir hata ortaya çıktı. Hatanın kaynağını tespit etmek için **Personel eylemleri mesaj günlüğünü** açın.
- **Engellendi** – Eylem talebi onaylayıcı tarafından engelledi.

## <a name="can-i-delete-a-personnel-action"></a>Bir personel eylemini silebilir miyim?
Evet, **Taslak**, **Hata**, **Başarısız** veya **İptal edilmiş** durumuna sahip personel eylemlerini silebilirsiniz. Yalnızca **Tamamlandı** durumundaki çalışanların eylemlerini , yalnızca **İnsan kaynakları paylaşılan parametreleri** sayfasında **Tamamlanan çalışan eylemlerini silmeye izin ver**'i **Evet** olarak ayralamış olmanız durumunda silebilirsiniz.

## <a name="what-is-the-fastest-way-to-check-the-status-of-a-personnel-action-request"></a>Bir personel eylemi talebinin durumunu denetlemenin en hızlı yolu nedir?
**Personel eylemi** listesi sayfalarından herhangi birini açın ve bir personel eylemi seçin.

## <a name="what-should-i-do-if-a-personnel-action-request-fails"></a>Bir personel eylemi talebi başarısız olursa ne yapmalıyım?
Bir personel eylemi talebi başarısız olursa, hatayı çözümlemek ve talebi yeniden göndermek için şu adımları izleyin:

> 1. Sorunu açıklayan ileti metnini görmek için **Eylem Bölmesi** üzerinde **Hata metni** düğmesine tıklayın.
> 
> 2. **Eylem Bölmesi** üzerinde, en güncel bilgiyi yüklemek ve personel eyleminin durumunu **Taslak**'a geri çevirmek için **Yeniden etkinleştir** üzerine tıklayın.
> 
> 3. Hatayı çözümleyin ve sonra **Tamamlandı** veya **Gönder** üzerine tıklayın.

## <a name="what-happens-to-a-personnel-action-that-uses-workflow-when-the-final-approval-is-completed"></a>Son onay tamamlandığında iş akışı kullanan bir personel eylemine ne olur?
Bir hata yoksa, personel eylemi salt okunur olur. (Geçmişi **Tüm çalışan eylemleri** liste sayfasında görebilirsiniz ancak personel eylemini değiştiremezsiniz.) Personel eyleminin durumu **Tamamlandı** ise, pozisyon veya çalışan kaydı zaten güncelleştirilmiştir. Gerçekleştirilen değişiklikleri görüntülemek için **Pozisyonlar** veya **Çalışanlar** liste sayfasını açın.

## <a name="why-do-i-receive-the-following-error-when-i-enter-a-non-zero-value-in-the-pay-rate-field-the-value-is-out-of-its-valid-range--it-much-be-between-000-and-000"></a>Ödeme oranı alanında sıfır olmayan bir değer girdiğimde neden aşağıdaki hatayı alıyorum? "Değer geçerli aralığın dışında – 0,00 ve 0,00 arasında olmalıdır"
Bu mesajı alıyorsunuz çünkü **İş** sayfasında bulunan **Düzey** alanı, seçilen konum ile ilişkilendirilmiş iş için boş.

Bu hatayı gidermek için şu adımları izleyin:

> 1. **Çalışan pozisyonu atama** sayfası üzerinde **Pozisyon** alanına tıklayın.  
> 2. **İş** sayfasını açmak için **İş** alanı değerine tıklatın.
> 3. Eylem bölmesinde, **Düzenle** öğesine tıklayın.
> 4. **Ücret** sekmesini tıklatın.
> 5. **Düzey** alanında bir düzey seçin.
> 6. **İş** sayfasını kapatın.
> 7. **Pozisyon** sayfasını kapatın.
> 8. **Çalışan** sayfasındaki **Ücret** sekmesine dönün ve **Sabit ücreti** seçin.  **Yeni**'yi seçin ve personelin pozisyonunu **Pozisyon** alanına girin.  **Plan** bölümünde bir değer girin ve daha sonra personelin ücretini **Ödeme oranı** alanına girin.

## <a name="why-cant-i-change-the-effective-date-on-the-header-of-the-worker-action-page"></a>Çalışan eylemi sayfasının başlığındaki yürürlük tarihini neden değiştiremiyorum?
Eylem türü için en mantıksal tarih ile doldurulmuş olduğu için yürürlük tarihini değiştiremezsiniz.

Örnek olarak:

- Bir **Çalışanı işten çıkar** eyleminin başlığındaki yürürlük tarihi, **İşten ayırma tarihi** alanına girdiğiniz tarihtir.
- Bir **Çalışanı işe al** eyleminin başlığındaki yürürlük tarihi, **İş başlangıç tarihi** alanına girmiş olduğunuz tarihtir.
- Bir **Çalışanı transfer et** eyleminin başlığındaki yürürlük tarihi, çalışan için **Atama başlangıç tarihi** alanına girmiş olduğunuz tarihtir.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
