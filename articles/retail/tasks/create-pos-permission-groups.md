---
title: POS izin grupları oluşturma
description: Bu konu POS izin grubunun nasıl oluşturulacağını açıklar.
author: scott-tucker
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e6782c60aa659523775cc6c4eb1694430a4bf4f
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914847"
---
# <a name="create-pos-permission-groups"></a>POS izin grupları oluşturma

[!include[task guide banner](../includes/task-guide-banner.md)]

Bu konu POS izin grubunun nasıl oluşturulacağını açıklar. Bu görevi oluşturmak için kullanılan demo verisi şirketi USRT'dir. Bu görev, Perakende operasyonları yöneticisi rolü için hazırlanmıştır.

1. Gezinti bölmesinde **Modüller > Perakende > Personel > İzin grupları**'na gidin.
2. **Yeni**'yi seçin.
3. **POS izin grubu kimliği** alanına bir değer yazın.
4. **Tanım** alanına bir değer girin.
5. **Saat girişlerini gör** alanında **Evet**'i seçin. Artık POS İzin grubunuz için çeşitli izinleri etkinleştirebilir veya devre dışı bırakabilirsiniz. Bazı izinler için POS kullanıcısının eylemi gerçekleştirip gerçekleştiremeyeceğini değerlendirmek amacıyla kullanılacak bir değer ayarlayabilirsiniz. Bu görev kılavuzu bir kasiyere verilebilecek bazı izinleri etkinleştirir.  
6. **Sipariş oluşturmaya izin ver** alanında **Evet**'i seçin.
7. **Siparişi düzenlemeye izin ver** alanında **Evet**'i seçin.
8. **Sipariş almaya izin ver** alanında **Evet**'i seçin.
9. **Parola değiştirmeye izin ver** alanında **Evet**'i seçin.
10. **Tamamen kapatmaya izin ver** alanında **Evet**'i seçin.
11. **Kaydet**'i seçin. Değişiklikleriniz kaydedildikten sonra, değişiklikleri perakende kanallarına itmek için Personel dağıtım planlamasını çalıştırmanız gerekir. 
12. Gezinti bölmesinde **Modüller > İnsan kaynakları > İşler > İşler**'e gidin.
13. Daha sonra, POS izin grubunu bir İşe atarız. Listede, istenen kaydı bulun ve seçin.
14. **Düzenle** öğesini seçin.
15. **İş sınıflandırma** bölümünü genişletin.
16. POS izin grubu alanına bir değer girin veya buradan bir değer seçin. Bu İşle ilgili Konumlarda bulunan tüm Çalışanlar, çalışanların POS izinleri Konum düzeylerinde geçersiz kılınmadığı sürece bu POS izin grubu ayarlarını kullanır.  
17. **Kaydet**'i seçin. Değişiklikleriniz kaydedildikten sonra, değişiklikleri perakende kanallarına itmek için Personel dağıtım planlamasını çalıştırmanız gerekir.  

