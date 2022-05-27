---
title: Kullanılabilen bütçe fonları
description: Bu konu, kullanılabilir bütçe fonları özelliğini tanıtır ve kuruluşunuzun mali kaynaklarının yönetimini en iyi duruma getirmek için bütçe denetimini yapılandırmanıza yardımcı olabilecek bilgiler sağlar.
author: RyanCCarlson2
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom:
- "60493"
- intro-internal
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2021-11-28
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: 1e7b2bf7ef7bd1bca6db27371f87dfddcdceef89
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710263"
---
# <a name="budget-funds-available"></a>Kullanılabilen bütçe fonları

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu konu, kullanılabilir bütçe fonları özelliğini tanıtır ve kuruluşunuzun mali kaynaklarının yönetimini en iyi duruma getirmek için bütçe denetimini yapılandırmanıza yardımcı olabilecek bilgiler sağlar.

## <a name="enhanced-calculation-feature-for-budget-funds-available"></a>Kullanılabilir bütçe fonları için geliştirilmiş hesaplama özelliği

**Yalnızca kullanılabilir bütçe fonları hesaplamasındaki tutarları izle** özelliği, **Bütçe denetim parametrelerini tanımla** sayfasındaki ayarlara bağlı olarak belge türleri ve durumları için temel bütçe denetim tablolarını izlemenizi sağlar.

Bazı bütçe denetimi yapılandırma seçeneklerinin özelliğin düzgün çalışması için belirli ayarlara sahip olması gerekir. Bu seçenekler, **Bütçe denetim parametrelerini tanımla** sayfasının **Kullanılabilir bütçe fonları** sekmesinde seçilir veya temizlenir. Aşağıdaki tabloda, kullanılabilir bütçe fonları özelliği için gereken ayarlar gösterilmektedir.

| Bu seçenek seçilidir | Bu seçenek de seçilmelidir |
| ------------------------- | -------------------------------- |
| Ön yükümlülükler için ayrılan bütçe rezervasyonları | Taahhütler *ve* Gerçek harcamalar için bütçe ayırmalar |
| Yükümlülükler için ayrılan bütçe rezervasyonları | Gerçek harcamalar |
| Satınalma Talebi türü belgeleriyle taahhütler için bütçe ayırmalar | Ön yükümlülükler için ayrılan bütçe rezervasyonları |

Bu özellik yalnızca yeni belgeleri etkiler. Mevcut belgelerin tutarları, kullanılabilir bütçe fonları ayarı değiştirilene ve yeni bütçe denetimi yapılandırması etkinleştirilene kadar izlenmeye ve bütçe denetimi istatistikleri sorgusunda gösterilmeye devam eder. Bu noktada, kullanılabilir bütçe fon hesaplamasından kaldırılan belgeler için bütçe izleme verileri kaldırılacaktır.

**Deftere nakledilmemiş gerçek harcamalar** seçeneğinin işaretini kaldırmanızı öneririz. Seçilirse bekleyen satıcı faturaları gibi deftere nakledilmemiş belgelerde zaman alan bir bütçe denetimi hesaplaması yapılır.
