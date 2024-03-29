---
title: POS izin grupları oluşturma
description: Bu makale POS izin grubunun nasıl oluşturulacağını açıklar.
author: josaw1
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.industry: Retail
ms.search.form: RetailPosPermissionGroup, HcmJob
ms.openlocfilehash: 0aa394e5dc6685954c31cdddae7cdc042b80af29
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277973"
---
# <a name="create-pos-permission-groups"></a>POS izin grupları oluşturma

[!include [banner](../includes/banner.md)]

Bu makale POS izin grubunun nasıl oluşturulacağını açıklar. Bu görevi oluşturmak için kullanılan demo verisi şirketi USRT'dir. Bu görev, Commerce operasyonları yöneticisi rolü için hazırlanmıştır.

1. Gezinti bölmesinde **Modüller > Retail and Commerce > Personel > İzin grupları**'na gidin.
2. **Yeni**'yi seçin.
3. **POS izin grubu kimliği** alanına bir değer yazın.
4. **Tanım** alanına bir değer girin.
5. **Saat girişlerini gör** alanında **Evet**'i seçin. Artık POS İzin grubunuz için çeşitli izinleri etkinleştirebilir veya devre dışı bırakabilirsiniz. Bazı izinler için POS kullanıcısının eylemi gerçekleştirip gerçekleştiremeyeceğini değerlendirmek amacıyla kullanılacak bir değer ayarlayabilirsiniz. Bu görev kılavuzu bir kasiyere verilebilecek bazı izinleri etkinleştirir.  
6. **Sipariş oluşturmaya izin ver** alanında **Evet**'i seçin.
7. **Siparişi düzenlemeye izin ver** alanında **Evet**'i seçin.
8. **Sipariş almaya izin ver** alanında **Evet**'i seçin.
9. **Parola değiştirmeye izin ver** alanında **Evet**'i seçin.
10. **Tamamen kapatmaya izin ver** alanında **Evet**'i seçin.
11. **Kaydet**'i seçin. Değişiklikleriniz kaydedildikten sonra, değişiklikleri Commerce kanallarına iletmek için Personel dağıtım planlamasını çalıştırmanız gerekir. 
12. Gezinti bölmesinde **Modüller > İnsan kaynakları > İşler > İşler**'e gidin.
13. Daha sonra, POS izin grubunu bir İşe atarız. Listede, istenen kaydı bulun ve seçin.
14. **Düzenle** öğesini seçin.
15. **İş sınıflandırma** bölümünü genişletin.
16. POS izin grubu alanına bir değer girin veya buradan bir değer seçin. Bu İşle ilgili Konumlarda bulunan tüm Çalışanlar, çalışanların POS izinleri Konum düzeylerinde geçersiz kılınmadığı sürece bu POS izin grubu ayarlarını kullanır.  
17. **Kaydet**'i seçin. Değişiklikleriniz kaydedildikten sonra, değişiklikleri kanallara iletmek için Personel dağıtım planlamasını çalıştırmanız gerekir.  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
