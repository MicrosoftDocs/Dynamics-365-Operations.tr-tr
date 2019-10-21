---
title: Ödünç verme maddeleri oluştur
description: Ödünç verilen maddeler, telefonlar veya bilgisayarlar gibi şirketinizin çalışanlarına ödünç verdiği fiziksel öğeleri izlemek için yardımcı kayıtlardır.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmLoanType, DefaultDashboard, HcmLoanItem, HcmWorkerLookUp
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 75b2f17eb41ead7422276f72429eb6ede2ef4759
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180451"
---
# <a name="create-loan-items"></a>Ödünç verme maddeleri oluştur

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ödünç verilen maddeler, telefonlar veya bilgisayarlar gibi şirketinizin çalışanlarına ödünç verdiği fiziksel öğeleri izlemek için yardımcı kayıtlardır. Her fiziksel öğeye karşılık gelen bir ödünç verilen madde olmalıdır. Ödünç verilen her madde kaydı, neyin ödünç verildiği, ödünç verme işleminden kimin sorumlu olduğu ve maddenin ödünç verilebileceği gün sayısını açıklamalıdır. Aynı anda birden fazla ödünç verilen maddeler, anahtar, erişim kartı veya üniforma gibi oluşturabilirsiniz. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="create-loan-types"></a>Ödünç verme türleri oluşturma
1. İnsan Kaynakları > Çalışanlar > Ödünç maddeler > Ödünç verme türleri seçeneğine gidin.
2. Yeni'ye tıklayın.
3. Ödünç verme türü alanına bir değer yazın.
4. Açıklama alanına bir değer girin.
5. Bu ödünç verme türüne atanan maddelerin süresinin geçebileceği gün sayısını girin. 
6. Kaydet'e tıklayın.
7. Sayfayı kapatın.
8. Sayfayı yenileyin.

## <a name="create-loan-items"></a>Ödünç verme maddeleri oluşturun
1. İnsan Kaynakları > Çalışanlar > Ödünç maddeler > Ödünç verilen maddeler seçeneğine gidin.
2. Ödünç verilen maddeler oluşturma'ya tıklayın.
3. Miktar'da bir sayı girin.
4. Açıklama alanına bir değer girin.
5. Ödünç verme türü alanında, aramayı açmak için açılır menü düğmesine tıklayın.
6. Listede, istenen kaydı bulun ve seçin.
7. Listede, seçili satırdaki bağlantıya tıklayın.
8. Maddenin ödünç verilebileceği gün sayısını girin.
    * Ödünç verilen ekipman sayfasındaki Planlanan iade alanında bulunan varsayılan değer geçerli tarih ve bu sayı toplanarak hesaplanır.  
9. Sorumlu kişi alanında, aramayı açmak için açılır menü düğmesine tıklayın.
10. Seç'e tıklayın.
11. Başlangıç değeri alanına bir numara girin.
12. Aralık alanına bir sayı girin.
13. Biçim alanına bir değer yazın.
    * Örneğin, ödünç verilen madde için başlangıç numarası 10 ise, Biçim alanında iki sayı sembolü girin.  
14. Tamam'a tıklayın.
15. Sayfayı yenileyin.

