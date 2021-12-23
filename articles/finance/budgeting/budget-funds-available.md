---
title: Kullanılabilen bütçe fonları
description: Bu konu, kullanılabilir bütçe fonları özelliğini tanıtır ve kuruluşunuzun mali kaynaklarının yönetimini en iyi duruma getirmek için bütçe denetimini yapılandırmanıza yardımcı olabilecek bilgiler sağlar.
author: rcarlson
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "60493"
- intro-internal
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2021-11-28
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: a8279ae9b08c7537548c1c8b71e6e978fee2b8a1
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891332"
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
