---
title: Ödünç verme maddeleri oluştur
description: Ödünç verilen maddeler, telefonlar veya bilgisayarlar gibi şirketinizin çalışanlarına ödünç verdiği fiziksel öğeleri izlemek için yardımcı kayıtlardır.
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmLoanType, DefaultDashboard, HcmLoanItem, HcmWorkerLookUp, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26bf5a83a6d25e99996ec4219c5fbbeed806e22d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693738"
---
# <a name="create-loan-items"></a>Ödünç verme maddeleri oluştur


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Ödünç verilen maddeler, telefonlar veya bilgisayarlar gibi şirketinizin çalışanlarına ödünç verdiği fiziksel öğeleri izlemek için yardımcı kayıtlardır. Her fiziksel öğeye karşılık gelen bir ödünç verilen madde olmalıdır. Ödünç verilen her madde kaydı, neyin ödünç verildiği, ödünç verme işleminden kimin sorumlu olduğu ve maddenin ödünç verilebileceği gün sayısını açıklamalıdır. Aynı anda birden fazla ödünç verilen maddeler, anahtar, erişim kartı veya üniforma gibi oluşturabilirsiniz. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="create-loan-types"></a>Ödünç verme türleri oluşturma
1. **İnsan Kaynakları** > **Çalışanlar** > **Ödünç maddeler** > **Ödünç verme türleri** seçeneğine gidin.
2. **Yeni**'yi tıklatın.
3. **Ödünç verme türü** alanına bir değer yazın.
4. **Tanım** alanına bir değer girin.
5. Bu ödünç verme türüne atanan maddelerin süresinin geçebileceği gün sayısını girin. 
6. **Kaydet**'e tıklayın.
7. Sayfayı kapatın.
8. Sayfayı yenileyin.

## <a name="create-loan-items"></a>Ödünç verme maddeleri oluşturun
1. **İnsan Kaynakları** > **Çalışanlar** > **Ödünç maddeler** > **Ödünç verilen maddeler** seçeneğine gidin.
2. **Ödünç verilen maddeler oluşturma**'ya tıklayın.
3. **Miktar**'da bir sayı girin.
4. **Tanım** alanına bir değer girin.
5. **Ödünç verme türü** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
6. Listede, istenen kaydı bulun ve seçin.
7. Listede, seçili satırdaki bağlantıya tıklayın.
8. Maddenin ödünç verilebileceği gün sayısını girin.
    * Ödünç verilen ekipman sayfasındaki Planlanan iade alanında bulunan varsayılan değer geçerli tarih ve bu sayı toplanarak hesaplanır.  
9. **Sorumlu kişi** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
10. **Seç**'e tıklayın.
11. **Başlangıç değeri** alanına bir numara girin.
12. **Aralık** alanına bir sayı girin.
13. **Biçim** alanına bir değer yazın.
    * Örneğin, ödünç verilen madde için başlangıç numarası 10 ise, **Biçim** alanında iki sayı sembolü girin.  
14. **Tamam**'a tıklayın.
15. Sayfayı yenileyin.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
