---
title: Çalışma süresi şablonları oluşturma
description: Çalışma zamanı şablonları bir haftalık çalışma saatlerini tanımlar ve bir dönem için çalışma zamanları oluşturmak için kullanılır.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 130a21d08e4e720f8bf803a5d4b03d315cefc26f
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580684"
---
# <a name="create-working-time-templates"></a>Çalışma süresi şablonları oluşturma

[!include [banner](../../includes/banner.md)]

Çalışma zamanı şablonları bir haftalık çalışma saatlerini tanımlar ve bir dönem için çalışma zamanları oluşturmak için kullanılır. Bu yordam, çalışma zaman aralıklarını kategorilere ayırmak için çalışma zamanı planlama özelliklerini kullanarak bir çalışma zamanı şablonunun nasıl tanımlanacağını gösterir. Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz.

1. **Çalışma alanları > Kaynak yaşam döngüsü yönetimi**'ne gidin.
1. **Çalışma zamanı şablonları**'nı seçin.

## <a name="create-working-time-template"></a>Çalışma zamanı şablonu oluşturma

1. **Yeni**'yi seçin.
1. **Çalışma zamanı şablonu** alanında bir değer girin.
1. **Ad** alanına bir değer yazın.
1. **Pazartesi** bölümünü genişletin.
1. **Ekle**'yi seçin.
1. **Başlangıç** alanında bir saat girin.
    * İşin sabah başlayacağı saati belirtin.  
1. **Bitiş** alanında bir saat girin.
    * Çalışanların öğle yemeği saatini belirtin.  
1. **Ekle**'yi seçin.
1. **Başlangıç** alanında bir saat girin.
    * Öğle yemeğinin ardından işin başlayacağı saati belirtin.  
1. **Bitiş** alanında bir saat girin.
    * İşin bitiş tarihini belirtin.  

## <a name="replicate-working-times-to-all-week-days"></a>Çalışma saatlerini haftanın tüm günleri için çoğaltma

1. **Kopyalama günü**'nü seçin.
    * Çalışma saati tanımlarını Pazartesi gününden Salı gününe kopyalayın.  
1. **Tamam**'ı seçin.
1. **Kopyalama günü**'nü seçin.
    * Çalışma saati tanımlarını Pazartesi gününden Çarşamba gününe kopyalayın.  
1. **Hafta içi bitiş tarihi** alanında bir seçenek belirleyin.
1. **Tamam**'ı seçin.
1. **Kopyalama günü**'nü seçin.
    * Çalışma saati tanımlarını Pazartesi gününden Perşembe gününe kopyalayın.  
1. **Hafta içi bitiş tarihi** alanında bir seçenek belirleyin.
1. **Tamam**'ı seçin.
1. **Kopyalama günü**'nü seçin.
    * Çalışma saati tanımlarını Pazartesi gününden Cuma gününe kopyalayın.  
1. **Hafta içi bitiş tarihi** alanında bir seçenek belirleyin.
1. **Tamam**'ı seçin.

## <a name="define-time-slots-for-special-operations"></a>Özel işlemler için zaman dilimi tanımlama

1. **Cuma** bölümünü genişletin.
1. Listede, istenen kaydı bulun ve seçin.
1. **Özellik** alanında bir değer girin veya bir değer seçin.
1. Listede, istenen kaydı bulun ve seçin.
1. **Özellik** alanında bir değer girin veya bir değer seçin.

## <a name="mark-weekend-days-as-closed-for-pickup"></a>Haftasonlarını malzeme çekme için kapatıldı olarak işaretleme

1. **Cumartesi** bölümünü genişletin.
1. **Malzeme çekme için kapatıldı** alanında *Evet* seçeneğini belirleyin.
1. **Pazar** bölümünü genişletin.
1. **Malzeme çekme için kapatıldı** alanında *Evet* seçeneğini belirleyin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]