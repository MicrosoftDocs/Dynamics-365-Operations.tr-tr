---
title: Eğitim kursları ayarlama
description: İnsan Kaynakları yöneticileri ve yöneticileri, kursları özelliğini kullanarak işçilere sunulan eğitim hakkındaki bilgileri tutabilirler.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 3e0a13d0b1882e6160a05925d97ecd85f1edfbaa
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "306583"
---
# <a name="set-up-training-courses"></a>Eğitim kursları ayarlama

[!include [banner](includes/banner.md)]

İnsan Kaynakları yöneticileri ve yöneticileri, kursları özelliğini kullanarak işçilere sunulan eğitim hakkındaki bilgileri tutabilirler.

 <a name="set-up-prerequisites"></a>Önkoşulları ayarlama
---------------------

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
- Çalışan self servis portalında daha sonra ilan edebileceğiniz bir kurs açıklaması oluşturma

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
Kurs katılımcıları, bir eğitim kursuna veya etkinliğe katılım gösteren çalışanlar, başvuranlar veya ilgili kişilerdir. Yalnızca açık kurslara katılımcıları kayıt yaptırabilirsiniz. Bir kursa kaydedebileceğiniz en az ve en çok katılımcı sayısı, **Kurslar** sayfasının **Genel** hızlı sekmesinde tanımlanır.

<a name="workflow"></a>İş Akışı
--------

**Personel self servis** sayfası üzerinden bir kursa kayıt olan personeller, kayıtlarını onay için çalışma akışından yönlendirebilirler.  Bir iş akışı, **Kurslar** sayfasında **Genel** hızlı sekmesinde bir kursa atanabilir.





