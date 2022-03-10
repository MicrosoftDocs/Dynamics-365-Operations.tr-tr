---
title: Eğitim kursları ayarlama
description: İnsan Kaynakları yöneticileri ve yöneticileri, kursları özelliğini kullanarak işçilere sunulan eğitim hakkındaki bilgileri tutabilirler.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: c66459a044419535d66875cddac7eb73af744ca7
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066762"
---
# <a name="set-up-training-courses"></a>Eğitim kursları ayarlama


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

İnsan Kaynakları yöneticileri ve yöneticileri, kursları özelliğini kullanarak işçilere sunulan eğitim hakkındaki bilgileri tutabilirler.

##  <a name="set-up-prerequisites"></a>Önkoşulları ayarlama

Aşağıdaki bilgiler gereklidir ve kurslar oluşturmadan önce ayarlanmış olması gerekir.
-   **Kurs tipleri**

Aşağdaki bilgiler kurslar için belirtebileceğiniz isteğe bağlı bilgilerdir. Kurslar için bu bilgiyi gireceğinizi biliyorsanız, bu bilgileri kurs kayıtlarını oluşturmadan önce ayarlamalısınız.
-   **Derslik grupları**
-   **Kurs grupları**
-   **Kurs yerleşimleri**
-   **Derslikler**
-   **Eğitmenler**

## <a name="course-types"></a>Kurs türleri
Kurs yapısı veya kurs içeriğine göre kategorilere ayırmak için Kurs türlerini kullanabilirsiniz. **Kurs türleri** sayfasın kurs türlerini oluşturabilirsiniz. Bir kurs kaydı oluştururken bir kurs türü seçmeniz gerekmektedir.

## <a name="course-setup-type"></a> Kurs kurulum türü
Kurslar için üç kurulum türü aşağıdaki tabloda listelenmektedir. Kursun yapısını kurulum türleri belirler.

<table>
<thead>
<tr class="header">
<th>Kurulum türü</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Standart</strong></td>
<td>Günlük bir gündemi olmayan kurslar için bu türü seçin. Yeni bir kurs oluşturduğunuzda, bu varsayılan türdür şeklindedir.</td>
</tr>
<tr class="even">
<td><strong>Ajanda</strong></td>
<td>Birden fazla gün sürecek kurs için her günün detayını planlamak için bu türü seçin.</td>
</tr>
<tr class="odd">
<td><strong>Gündem + oturumlar</strong></td>
<td>Daha karmaşık kurslar için bu türü seçin. Örneğin kursun gündemini parçalara ve oturumlara bölebilirsiniz.
<ul>
<li><strong>Parça</strong> – Parçalar bir kurs için belirli konu alanlarıdır.</li>
<li><strong>Oturumlar</strong> – Oturumlar parçaları böler ve parçaya ilişkin işlemlerin veya tekniklerin tanımlanmasında yardımcı olur.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a> Kurs görevleri
Her kurs için aşağıdaki görevleri yerine getirebilirsiniz:
- Katılımcı kaydetme
- Kayıt için süre sonu belirleme
- Katılımcılar için en az ve en fazla sayı belirleme
- Bir kurs yeri ve sınıfı atama
- Kurs katılımcılarına otel önerme
- **Personel self servisi**'nde daha sonra ilan edebileceğiniz bir kurs açıklaması oluşturma

  >**Not** Kursu sadece kimse kayıt olmadıysa silebilirsiniz. 

## <a name="course-statuses"></a>Kurs durumları
Aşağıdaki tabloda olası kurs durumları ve kursun belirli bir durumu varsa tamamlayabilmeniz için eylemler listelenir.

<table>
<thead>
<tr class="header">
<th>Durum</th>
<th>Eylemler</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Oluşturuldu</strong></td>
<td><ul>
<li>Kurs bilgilerini girin ve değiştirin.</li>
<li>Kursun durumunu <strong>Açık</strong> olarak değiştirin ve böylece çalışanların kurs için kayıt yaptırabilir.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Aç</strong></td>
<td><ul>
<li>Kurs için katılımcılar kaydedin.</li>
<li>Kurstan katılımcı çıkartın.</li>
<li>Kurs için katılımcılar teyit edin.</li>
<li>Kursun durumunu <strong> Kapalı</strong> veya <strong>İptal edildi</strong> değiştirin.</li>
<li>Durumu <strong>Onaylandı</strong> olan katılımcılar için soru formları planlayın.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Kapalı</strong></td>
<td>Kursu yeniden açabilirsiniz.</td>
</tr>
<tr class="even">
<td><strong>İptal edildi</strong></td>
<td>Kursu yeniden açabilirsiniz.</td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a>Kurs katılımcıları
Kurs katılımcıları, bir eğitim kursuna veya etkinliğine katılım gösteren çalışanlardır. Yalnızca açık kurslara katılımcıları kayıt yaptırabilirsiniz. Bir kursa kaydedebileceğiniz en az ve en çok katılımcı sayısı, **Kurslar** sayfasının **Genel** hızlı sekmesinde tanımlanır.

## <a name="workflow"></a>İş Akışı

**Personel self servis** sayfası üzerinden bir kursa kayıt olan personeller, kayıtlarını onay için çalışma akışından yönlendirebilirler. Bir kursu bir iş akışına, **Kurslar** sayfasında **Genel** hızlı sekmesinden atayabilirsiniz.







[!INCLUDE[footer-include](../includes/footer-banner.md)]
