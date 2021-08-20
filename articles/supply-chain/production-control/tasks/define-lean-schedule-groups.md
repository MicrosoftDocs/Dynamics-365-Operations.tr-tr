---
title: Yalın planlama gruplarını tanımlama
description: Yalın planlama grupları, ürünleri kanban planlamada gruplamak ve ayırt etmek için tanımlanır.
author: cvocph
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanScheduleGroup, GanttColorTableLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4187381b838825b21a354eeecdf48693d919975b07a881ba32d234135694ad06
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754596"
---
# <a name="define-lean-schedule-groups"></a>Yalın planlama gruplarını tanımlama

[!include [banner](../../includes/banner.md)]

Yalın planlama grupları, ürünleri kanban planlamada gruplamak ve ayırt etmek için tanımlanır. Gruplandırma, şirket başına genel bir ilişkilendirmeyle veya belirli bir iş hücresine özgü olarak yapılabilir. Kanban planlama liste sayfasında görsel bir gösterge olması amacıyla her grup için atanmış bir renk kodu vardır. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="define-lean-scheduling-group"></a>Yalın planlama grubunu tanımlama
1. Ürün bilgileri yönetimi > Yalın imalat > Kanban planlama kuralları'na gidin.
2. Yeni'ye tıklayın.
3. Zamanlama grubu alanında bir değer girin.
    * Zamanlama grubu, genel grup olarak veya belirli bir iş hücresine özgü şekilde tanımlanabilir. Bu basit örnekte, genel bir grup tanımlanmıştır ve iş hücresi boş tutulur. Bu grubun ayarları, belirli zamanlama grupları olmayan tüm iş hücreleri için geçerlidir.  
4. Renk seçiminden bir renk seçin.
    * Renkler, kanban zamanlama listesi sayfasındaki veya kanban işlem panosundaki işleri vurgulamak için kullanılır.  
5. Listede, seçili satırı işaretleyin.
6. Listede, seçili satırdaki bağlantıya tıklayın.

## <a name="associate-product"></a>Ürün ilişkilendirme
1. Belirli bir ürünle ilişkilendirme yapma
    * Yalın planlama gruplarıyla, belirli bir ürün (Ürün ilişkisi türü = Ürün) ya da bir ürün tahsisat anahtarının parçası olarak (Ürün ilişkisi türü = grup) ürün ilişkilendirmek için iki yol vardır.    
2. İlişki türü alanında Ürün öğesini seçin.
3. Madde numarası alanına bir değer girin.
4. İş çıkarma yeteneği oranı alanında bir sayı girin.
    * Varsayılan İş çıkarma yeteneği oranı 1'dir ve bunun anlamı ilgili ürünlerin üretim akışlarının işlem faaliyetlerinde belirtilen tam kapasiteyi tüketeceğidir. İş çıkarma yeteneği oranı > 1, daha yüksek kaynak tüketimi, İş çıkarma yeteneği oranı > 1 ise daha düşük bir kaynak tüketimi ifade edilir. Oran, maliyet hesaplamasında ve kanban işi tüketiminin hesaplanmasında kullanılır.  

## <a name="associate-item-allocation-key"></a>Ürün tahsisat anahtarını ilişkilendirme
1. Ürün tahsisat anahtarını ilişkilendirme
    * Ürün ilişki türü Grubu kullanarak bir ürün tahsisat anahtarına bir ilişki ekleyin.   Bu işlem için verilerinizde tanımlanan bir tahmini ürün tahsisatı anahtarı gerektiğini unutmayın.  
2. İlişki türü alanında Grup öğesini seçin.
3. Ürün tahsisat anahtarı alanında, aramayı açmak için açılır menü düğmesini tıklatın.
4. Listede, seçili satırdaki bağlantıya tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]