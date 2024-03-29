---
title: Günlükler için gelişmiş kurallar oluşturma
description: Bu yordam, günlükler için gelişmiş kurallar oluşturmayı adım adım açıklar.
author: aprilolson
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f5cc41f19928fd415fb54073fd733f97a3e7aa01
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717432"
---
# <a name="create-advanced-rules-for-journals"></a>Günlükler için gelişmiş kurallar oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordam, günlükler için gelişmiş kurallar oluşturmayı adım adım açıklar. Bu, günlük kontrolü ve kullanıcı deftere nakil kısıtlamalarını ayarlamayı içerir. Bu yordam, USMF demo verisi şirketini kullanır.


## <a name="set-up-journal-control"></a>Günlük kontrolünü ayarlama
1. **Gezinti bölmesinde** **Modüller > Genel muhasebe > Günlük kurulumu > Günlük adları**'na gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. **Eylem bölmesinde** **Günlük denetimi** öğesine tıklayın.
4. **Deftere nakledilebilecek hesap türleri** hızlı sekmesinde **Ekle**'ye tıklayın.
5. **Şirket hesapları** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
6. Listede, istenen kaydı bulun ve seçin.
7. Listede, seçili satırdaki bağlantıya tıklayın.
8. **Bu günlük için geçerli olan segment değerleri** hızlı sekmesinde **Ekle**'ye tıklayın.
9. **Hesap yapısı** alanında, aramayı açmak için açılır menü düğmesini tıklatın.
10. Listede, istenen kaydı bulun ve seçin.
11. Listede, seçili satırdaki bağlantıya tıklayın.
12. **Segment** alanında, aramayı açmak için açılır menü düğmesini tıklatın.
13. Listede, seçili satırdaki bağlantıya tıklayın.
14. **Başlangıç değeri** alanında, aramayı açmak için açılır menü düğmesini tıklatın.
15. Listede, istenen kaydı bulun ve seçin.
16. Listede, seçili satırdaki bağlantıya tıklayın.
17. **Bitiş değeri** alanında, aramayı açmak için açılır menü düğmesini tıklatın.
18. Listede, istenen kaydı bulun ve seçin.
19. Listede, seçili satırdaki bağlantıya tıklayın.

## <a name="set-up-posting-restrictions"></a>Nakil kısıtlamalarını ayarlama
1. Sayfayı kapatın.
2. **Deftere nakil kısıtlamaları**'nı tıklatın.
3. **Deftere nakil sınırlamalarını nasıl ayarlamak istiyorsunuz?** alanında 'Kullanıcı grubuna göre'yi seçin.
4. Ağaçta, 'Bu günlük adı için deftere nakile izin vermek istediğiniz grup' öğesini işaretleyin.
5. **Tamam**'a tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
