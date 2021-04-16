---
title: Kiralama kullanıcı rolleri atama
description: Bu konuda, Varlık kiralamada kullanılan güvenlik rolleri açıklanmıştır. Ayrıca, kullanıcıların bu rollere nasıl atanacağını da açıklanmıştır.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 16719576dde73f096c0102a89c43cbc75594cc80
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819854"
---
# <a name="assign-lease-user-roles"></a>Kiralama kullanıcı rolleri atama

[!include [banner](../includes/banner.md)]

Bu konuda, Varlık kiralamada kullanılan güvenlik rolleri açıklanmıştır. Ayrıca, kullanıcıların bu rollere nasıl atanacağını da açıklanmıştır.

Varlık kiralamada erişim izinlerini ayırmak için üç kullanıcı rolü bulunur. Bu rollerden biri kiralamaların bakımını yapmak, biri kiralamaları görüntülemek ve biri kiralama uzmanı görevlerini yerine getirmek için uygundur. Her rolün tüm kiralama sayfaları için özel izinleri vardır ve her biri, kullanıcıların iş sorumluluklarına göre kiralamaları görüntülemesine, oluşturmasına, düzenlemesine veya silmesine izin verir.

| Rol           | Tanım |
|----------------|-------------|
| Kiralama Bakımını Yapma | Bu roldeki kullanıcılar kiralama ekleyebilir, düzenleyebilir, silebilir ve görüntüleyebilir. Bu rol, aylık günlük girişleri oluşturma ve deftere nakletme ve yeni kiralama ekleme gibi görevleri olan günlük kullanıcılar için tasarlanmıştır. Bu rol, tüm Varlık kiralama işlevlerine erişim sağlar. |
| Kiralamayı Görüntüleme     | Bu roldeki kullanıcılar yalnızca kiralama kayıtlarını ve planları görüntüleyebilir ve raporları çalıştırabilir. Bu kullanıcılar yeni kiralamalar oluşturamaz, mevcut kiralamaları düzenleyemez veya kiralar için günlük girişleri oluşturamaz. Bu rol, yalnızca kiralamaları ve kira planlarını görüntülemesi ve bu kiralamalar için oluşan hareketleri görmesi gereken kullanıcılar için tasarlanmıştır. |
| Kiralama Memuru    | Bu roldeki kullanıcılar yalnızca yeni kiralamalar oluşturabilir. Mevcut kiraları düzenleyemez veya silemez, kira planlarını görüntüleyemez veya kira günlüğü girişlerini deftere nakledemez. Bu rol, veri girişi kapasitesiyle çalışan kullanıcılar için tasarlanmıştır. |

Varlık kiralamada kullanıcıları bu rollere atamak için bu adımları izleyin.

1. **Sistem Yönetimi \> Güvenlik \> Kullanıcılara roller atayın**'a gidin.
2. **Kiralama bakımını yapma**, **Kiralama memuru** veya **Kiralamayı görüntüleme** rolünü seçin ve ardından **Kullanıcıları el ile ata/dışarıda tut** seçeneğini belirleyin.
3. Role atanacak kullanıcıyı seçin ve **Role ata**'yı seçin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]