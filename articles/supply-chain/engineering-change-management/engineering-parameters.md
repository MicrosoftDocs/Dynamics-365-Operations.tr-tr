---
title: Mühendislik değişimi yönetimi parametreleri
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management için mühendislik değişikliği yönetimi özelliklerinin nasıl yapılandırılacağı açıklanmaktadır.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 0cf0e56a8aece98379aa0f181d7b7ff665767544
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/29/2020
ms.locfileid: "4439751"
---
# <a name="engineering-change-management-parameters"></a>Mühendislik değişimi yönetimi parametreleri

[!include [banner](../includes/banner.md)]

**Mühendislik değişikliği yönetimi parametreleri** sayfası, sürüm ürün yapısı ve mühendislik değişikliği yönetimi işlemleriyle ilgili varsayılan davranışı değiştiren kurulum parametreleri içerir.

## <a name="open-the-engineering-change-management-parameters-page"></a>Mühendislik değişikliği yönetimi parametreleri sayfasını açma

**Mühendislik değişikliği yönetimi parametreleri** sayfasını açmak için **Mühendislik değişikliği yönetimi \> Kurulum \> Mühendislik değişikliği yönetimi parametreleri** sayfasına gidin. Alanları, bu konunun geri kalan bölümlerinde açıklandığı gibi ayarlayabilirsiniz.

## <a name="release-control-tab"></a>Serbest bırakma denetimi sekmesi

Aşağıdaki tablo, **Mühendislik değişikliği yönetimi parametreleri** sayfasının **Serbest bırakma denetimi** sekmesinde kullanılabilen alanları tanımlar. Bu alanlar, ürün yapısını serbest bırakma işlemini etkiler.

| Alan | Tanım |
|---|---|
| Madde numarası kuralı | Ürün tüzel bir kişiliğe serbest bırakıldığında madde numarasının nasıl tanımlanacağını seçin. Alıcı tüzel kişilikteki ürün numarasının, mühendislik şirketindeki ürün numarasıyla eşleşmesi gerekiyorsa *Mühendislik ürün numarası*'nı seçin. Ürünün, alıcı tüzel kişiliğindeki ürün numaralarının numara serisindeki bir sonraki numarayı alması gerekiyorsa *Yerel madde numarası serisi*'ni seçin. |
| Ürün reçetesi adı kuralı | Ürün, bir tüzel kişilikte alındığında (serbest bırakıldığında) ürün reçetesi adının nasıl tanımlanacağını seçin. *Mühendislik adı* ya da *Teslim alma madde numarası*'nı seçin. |
| Rota adı kuralı | Bir ürünün rotası, bir tüzel kişilikte alındığında (serbest bırakıldığında) rota adının nasıl tanımlanacağını seçin. *Mühendislik adı* ya da *Teslim alma madde numarası*'nı seçin. |
| Ürün reçetesi denetimini çalıştır | Ürün tüzel bir kişilikte teslim alındığında (serbest bırakıldığında) bir ürün reçetesi denetiminin çalıştırılıp çalıştırılmayacağını seçin. |
| Etkin olmayan ürün reçetesini serbest bırakma davranışı | Etkin olmayan ürün reçetesi olan bir ürünün serbest bırakılabilir olup olmayacağını seçin. *Kabul Et*, *Yalnızca uyarı* veya *İzin verilmez*'i seçin. |
| Etkin olmayan rotayı serbest bırakma davranışı | Etkin olmayan rotası olan bir ürünün serbest bırakılabilir olup olmayacağını seçin. *Kabul Et*, *Yalnızca uyarı* veya *İzin verilmez*'i seçin.|
| Ürün kabulü | Ürünün tüzel kişiliğe serbest bırakılmadan önce kabul için ek bir adım gerekli olup olmayacağını belirleyin. Kabul adımını eklemek için *El ile*'yi seçin. Bu durumda, **Açık ürün serbest bırakmaları** sayfası ürünleri gösterir. Ürünü serbest bırakma ürün yapısı ile birlikte serbest bırakıldıktan hemen sonra hedef tüzel kişilikte doğrudan **Serbest bırakılan ürünler** sayfasında doğrudan görüntülemek için *Otomatik*'i seçin. |

## <a name="engineering-change-management-tab"></a>Mühendislik değişikliği yönetimi sekmesi

Aşağıdaki tablo, **Mühendislik değişikliği yönetimi parametreleri** sayfasının **Mühendislik değişikliği yönetimi** sekmesinde kullanılabilen alanları tanımlar. Bu ayarlar, mühendislik değişikliği yönetimi sürecini etkiler.

| Alan | Tanım |
|---|---|
| Kategori | Bir mühendislik değişikliği isteği oluşturulduğunda kullanılacak olan varsayılan kategori. |
| Öncelik | Bir mühendislik değişikliği isteği oluşturulduğunda kullanılacak olan varsayılan öncelik. |
| Önem derecesi kuralı | Mühendislik değişikliği emrinin önem derecesini seçin. Kullanıcının **Önem Derecesi** alanına bir değer girmesi bekleniyorsa *El ile* seçeneğini belirleyin. Mühendislik değişikliği emrinin Eylem bölmesinde **Önem derecesini hesapla** seçeneğini belirlediğinizde, sistemin **Önem Derecesi** alanındaki değeri hesaplamasını sağlamak için *Hesapla*'yı seçin. Bu durumda, sistem, **Önem derecesi kural kümesi** sayfasında tanımlanan önem derecesi kurallarını kullanır. **Önem derecesi** alanı değerinin otomatik olarak hesaplanıp önem derecesi kuralı kümelerine göre doldurulması için *Otomatik olarak hesapla*'yı seçin. |
| Etkilenen ürünleri yeniden serbest bırak | Bu alan, bir mühendislik değişikliği emri aracılığıyla ürünleri yeniden serbest bıraktığınızda kullanılabilir. **Serbest bırakmalar** iletişim kutusunda, tüm ürünlerin veya yalnızca etkilenen ürünlerin önerilip önerileceği arasında seçim yapabilirsiniz. |
| Serbest bırakılacak ürün reçetesi düzeyleri | Serbest bırakılacak ürün reçetesi düzeyi derinliği. Ürün reçetesinde burada belirtilen değerden daha fazla düzey varsa (daha derin ise), yalnızca belirtilen değer üzerindeki düzeyler serbest bırakılır. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]