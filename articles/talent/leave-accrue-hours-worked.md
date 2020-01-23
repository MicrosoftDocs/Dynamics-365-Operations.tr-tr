---
title: Çalışılan saatlere göre süre tahakkuk
description: Bu konu, bırakma planlarının çalışılan saatlere dayanarak süre tahakkuk edilmesini yapılandırmayı anlatır.
author: andreabichsel
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-09-17
ms.dyn365.ops.version: ''
ms.openlocfilehash: 938d2eea7b9e85b19e9c1e3e0930f625224b880d
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898631"
---
# <a name="accrue-time-off-based-on-hours-worked"></a>Çalışılan saatlere göre süre tahakkuk

## <a name="overview"></a>Genel bakış

Saatlik çalışanı olan kuruluşlar, kuruluştaki kıdem yerine çalışılan saatlere dayanarak izin verebilirler. Çalışılan saatler verisi genellikle bir zaman ve katılım sisteminde depolanır. Beceride: Core HR, normal ve fazla mesai çalışmaları içeri aktarılabilir ve bir personelin ikramiyesi olarak kullanılabilir.

## <a name="leave-plans"></a>İzin planları

İzin planı içerisinde, tahakkuk türü çalışılan saatler veya hizmet verilen aylar olabilir. Çalışılan saatler seçildiğinde, tahakkuk için kullanılacak iki saat türü vardır: normal ve fazla mesai.

Çalışma saatleri kullanmak için bir izin planı ayarlamak için şu adımları izleyin:

1. **İzin ve devamsızlık planları** sayfasında, **Yeni plan oluştur** üzerine tıklayın.
2. İzin planınız için bir ad girin.
3. Plan için tahakkuk sıklığını girin.
5. Plan başlangıç tarihini seçin.
6. Tahakkuk dönemi temelini seçin ve varsa personele özel tarihi seçin.
7. Tahakkuk planlaması için **Çalışılan saatler**'i tahakkuk türü için seçin.
8. Tahakkuk için kullanılacak saatlerin türünü seçin.
9. Çalışılan saatlerin sayısını ve bununla ilişkilendirilen tahakkuk miktarını, minimum bakiyeyi ve maksimum devretmeyi veya verilen tutarı girin.

Çalışılan saatler planları için tahakkuk işleme, tahakkuk sıklığını, tahakkuk dönemi tabanı ile kullanarak tahakkuk edilecek saatleri belirlemek için kullanır.

## <a name="annual-accrual-frequency"></a>Yıllık tahakkuk sıklığı

| Tahakkuk verilme tarihi    | Çalışılan saatler katmanı    | Tahakkuk tutarı        | Çalışan saatlerin tarihi   | Çalışılan gerçek saatler| İkramiye               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31/12/2018            | 2080                 | 144                   | 1/1/2018-31/12/2018  | 2085                | 144                 |        
| 31/12/2018            | 2080                 | 144                   | 1/1/2018-31/12/2018  | 2000                | 0                 |


## <a name="monthly-accrual-frequency"></a>Aylık tahakkuk sıklığı

| Tahakkuk verilme tarihi    | Çalışılan saatler katmanı    | Tahakkuk tutarı        | Çalışan saatlerin tarihi   | Çalışılan gerçek saatler| İkramiye               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 160                  | 12                    | 1/8/2018-31/8/2018   | 184                 | 12                  |        
| 31/8/2018             | 160                  | 3                     | 1/8/2018-31/8/2018   | 184                 | 3                   |

## <a name="semi-monthly-accrual-frequency"></a>Ayda iki kez tahakkuk sıklığı

| Tahakkuk verilme tarihi    | Çalışılan saatler katmanı    | Tahakkuk tutarı        | Çalışan saatlerin tarihi   | Çalışılan gerçek saatler| İkramiye               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31/8/2018             | 80                   | 6                     | 16/8/2018-31/8/2018  | 81                  | 6                  |        
| 31/8/2018             | 80                   | 6                     | 16/8/2018-31/8/2018  | 75                  | 0                   |

## <a name="weekly-accrual-frequency"></a>Haftalık tahakkuk sıklığı

| Tahakkuk verilme tarihi    | Çalışılan saatler katmanı    | Tahakkuk tutarı        | Çalışan saatlerin tarihi   | Çalışılan gerçek saatler| İkramiye               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31/8/2018             | 40                   | 3                     | 27/8/2018-31/8/2018  | 42                  | 3                  |        
| 31/8/2018             | 40                   | 3                     | 27/8/2018-31/8/2018  | 35                  | 0                   |

## <a name="employee-assigned-leave-plans"></a>Personel atanan izin planları

Personelin atanan izin planlarında, katman tabanı ve saatlerin türü, çalışılan saatlerin tahakkuk türü olarak tanımlandığı için gösterilir. Etkin planlar için gerçek tahakkuk dönemlerinin geçerli itibariyle çalışılan saatleri tarihi de başvuru için görüntülenir. 

## <a name="loading-data"></a>Veriler yükleniyor

Gerçek saatler, veri yönetimindeki izin ve devamsızlık saatleri çalışılan varlığı kullanılarak içe aktarılabilir. Çalışma saati takvimleri kullanıyorsanız, içe aktarma normal saatlerin takvim tarafından tanımlanan planlanmış saatleri aşmayacağı doğrulayacaktır. İçe aktarma ayrıca bir gündeki çalışılan saatlerin 24'ü geçmemesini de doğrular. 

Aşağıdaki bilgiler gerçek saatlerin izin tahakkuk işleminde kullanılabilmesi için içe aktarılmasında gereklidir:

+ Personel numarası 
+ Çalışılan tarih
+ Türü
+ Saatler

Tek bir tarih yalnızca bir tipi ilişkilendirilmiş olabilir.

| PERSONELNUMARASI       | ÇALIŞILANTARİH           | TÜR                  | SAATLER                |
| --------------------- | -------------------- | --------------------- | -------------------- |
| 000337                | 6/8/2018             | Normal               | 8                    |       
| 000337                | 7/8/2018             | Normal               | 8                    |
| 000337                | 7/8/2018             | Fazla mesai              | 3                    |
| 000337                | 8/8/2018             | Normal               | 8                    |
| 000337                | 7/8/2018             | Normal               | 8                    |
| 000337                | 9/8/2018             | Normal               | 8                    |
