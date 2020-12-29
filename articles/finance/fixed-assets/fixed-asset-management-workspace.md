---
title: Sabit kıymet yönetim çalışma alanı
description: Bu konu Sabit kıymet yönetimi çalışma alanı hakkında bilgiler sağlar. Bu çalışma alanı, sisteme girilen sabit kıymetlerle ilgili bilgileri gösterir. Bir özet görünümü ve bir analiz görünümü içerir.
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: ea6f04b1dad162749edc1ad7662f7d9cf077221d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448793"
---
# <a name="fixed-asset-management-workspace"></a>Sabit kıymet yönetim çalışma alanı

[!include [banner](../includes/banner.md)]

**Sabit kıymet yönetimi** çalışma alanı, sisteme girilen sabit kıymetlerle ilgili bilgileri gösterir. Bu çalışma alanı bir özet görünümü ve bir analiz görünümü içerir. **İşim** sekmesi özet kutucuklarını, sabit kıymet ayrıntılarını ve geçerli şirketteki sabit kıymetler ile ilgili bilgileri gösterir. Ayrıca, Power BI analizler bölümüne analizleri doğrudan çalışma alanı içinden ekleyebilirsiniz. **Analizler – tüm şirketler sekmesi**, tüm şirketlerle ilişkili sabit kıymetlerin görsellerini göstermek için Microsoft Power BI yeterliklerini kullanır.

## <a name="my-work"></a>İşim

### <a name="summary"></a>Özet

**Özet** bölümündeki kutucuklar, sabit kıymetlerinizin bir genel bakışını sağlar. Bilgi, henüz alınmamış olan varlıklar, mevcut yıl boyunca alınmış olan varlıklar ve mevcut yıl boyunca elden çıkarılmış varlıklar hakkında ölçümler içerir. **Özet** bölümü, **Sabit kıymet** liste sayfasına, toplu iş amortisman teklifine ve sabit kıymet günlüğüne hızlı geçişe sahiptir.

### <a name="find-fixed-assets"></a>Sabit kıymetleri bul

**Sabit kıymetler bul** bölümü, sabit kıymet numarası, grubu, adı, konumu ve sorumlusunu kullanarak varlıkları hızla aramanıza olanak sağlar. Arama kriteriyle eşleşen tüm varlıklar listede görünür.

Listeden, aşağıdaki sayfaları görüntüleyebilirsiniz:

 - Sabit kıymet için **Ayrıntılar** sayfası
 - Sabit kıymet ile ilişkilendirilmiş tüm defterler için **Defterler** sayfası
 - **Sabit kıymet değerlemeleri** sayfası

### <a name="valuations"></a>Değerlemeler

**Sabit kıymet değerlemeleri** sayfası, tek bir sayfa üzerinde, bir sabit kıymet hakkındaki en önemli bilgileri ve bu sabit kıymet ile ilişkilendirilmiş tüm defterlerin ayrıntılarını görmenizi sağlar. Sayfanın sol üstündeki **Bakiyeler** seçeneği, sabit kıymet ile ilişkilendirilmiş her bir defterin geçerli değerlemesini gösterir. Özet değerini oluşturan ayrıntılı hareketleri görmek için değerlerden ayrıntıya geri inebilirsiniz. Sayfanın sol üstündeki **Profil** seçeneği, sabit kıymet ile ilişkilendirilmiş her bir defterin amortisman planlamasını gösterir.

**Sabit kıymet değerlemeleri** sayfasına, **Sabit kıymet** liste sayfasında bulunan **Sabit kıymet yönetimi** çalışma alanından erişebilirsiniz.

### <a name="related-information"></a>İlgili bilgiler

Çalışma alanının **İlgili bilgi** bölümündeki bağlantıları kullanarak doğrudan **Defter kurulumu** sayfasına, **Sabit kıymet hareket sorgulaması** sayfasına ve çeşitli raporlara gidebilirsiniz.

### <a name="analytics--all-companies"></a>Analizler – tüm şirketler

**Analizler** sayfası, sistemdeki tüm tüzel varlıklardaki sabit kıymetler hakkında önemli ölçümleri sağlar. Bu sekmeye erişim, tüm şirketler için sabit kıymet analizlerini görüntüle güvenlik ayrıcalığı tarafından denetlenir.

Aşağıdaki tablo, her bir rapor sayfasında kullanılabilen görselleştirmeleri gösterir.

| Rapor sayfası            | Gözde canlandırma        |
|------------------------|----------------------|
| Sabit kıymet değerlemeleri | Toplam net defter değeri |
| Sabit kıymet değerlemeleri | Sabit kıymet grubuna göre net defter değerleri |
| Sabit kıymet değerlemeleri | Alım değerleri |
| Sabit kıymet değerlemeleri | Elden Çıkarma değerleri |
| Sabit kıymet değerlemeleri | Sabit kıymet ayrıntıları |
| Değerlemeler haritaları        | Toplam net defter değeri |
| Değerlemeler haritaları        | Sabit kıymet konumları |
| Değerlemeler haritaları        | Sabit kıymet ayrıntıları |

Analizi veri ile görüntülemek için önce AssetTransactionMeasure toplam ölçümünü **Varlık Deposu** sayfasında yenilemelisiniz.
