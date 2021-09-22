---
title: Giriş/çıkış noktası yönetimi profili kullanılırken karışık stok türleri
description: Giriş/çıkış noktası yönetim profilinin stok karıştırmayı etkin bir şekilde yönetmesi için öncelikle bir iş başlığı sonu ayarlanmalıdır. Bu sayfada, bunun nasıl yapılacağı açıklanmaktadır.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: cc660a2f9839e886240c97a7f60d2e264653074a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477832"
---
# <a name="inventory-types-are-being-mixed-when-using-a-dock-management-profile"></a>Giriş/çıkış noktası yönetimi profili kullanılırken stok türleri karıştırılıyor

## <a name="symptoms"></a>Belirtiler

*Sevkiyat konsolidasyonu ilkeleri*'ni kullanıyorsunuz. *Konum profili* için bir *giriş/çıkış noktası yönetim profili* ayarlayıp iş oluşturduğunuzda stok türleri son konumda karıştırılır.

## <a name="resolution"></a>Çözüm

Giriş/çıkış noktası yönetim profillerinin önceden bölünmesi için çalışma gerekir. Başka bir deyişle, giriş/çıkış noktası yönetim profili, bir iş başlığının birden çok yerleştirme konumuna sahip olmayacağını bekler.

Giriş/çıkış noktası yönetim profilinin stok karıştırmayı etkin bir şekilde yönetmesi için bir iş başlığı sonu ayarlanmalıdır.

Bu örnekte, giriş/çıkış noktası yönetim profilimiz **Karıştırılmaması gereken stok türleri** *Sevkiyat Kimliği* olarak ayarlanacak şekilde yapılandırılmıştır ve bunun için bir iş başlığı sonu ayarlayacağız:

1. **Ambar yönetimi \> Kurulum \> İş \> İş şablonları**'na gidin.
1. Düzenlenecek **İş emri türünü** seçin (örneğin, *Satın alma siparişleri*).
1. Düzenlenecek iş şablonunu seçin.
1. Eylem Bölmesi'nde, **Sorgu düzenle**'yi seçin.
1. **Sıralama** sekmesini açın ve aşağıdaki ayarlara sahip bir satır ekleyin:
    - **Tablo** - *Geçici iş hareketleri*
    - **Türetilmiş tablo** - *Geçici iş hareketleri*
    - **Alan** - *Sevkiyat Kimliği*
1. **Tamam**'ı seçin.
1. **İş şablonları** sayfasına yönlendirilirsiniz. Eylem Bölmesinde **İş başlığı sonları**'nı seçin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **Alan adı** *Sevkiyat Kimliği* ile ilişkili onay kutusunu seçin.
1. Eylem bölmesinde, **Kaydet**'i seçin.
