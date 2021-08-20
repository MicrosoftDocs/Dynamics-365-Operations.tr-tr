---
title: Teminat mektupları için banka hizmetlerini ve banka deftere nakil profillerini ayarlama
description: Bu görev, garanti mektubu işlemek için gereken banka tesisi ve deftere nakil profilini oluşturur.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1a7e60903e31d98e24f578dc381bb0b140944e07a88516a6a81bbba1b8981982
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742240"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a>Teminat mektupları için banka hizmetlerini ve banka deftere nakil profillerini ayarlama

[!include [banner](../../includes/banner.md)]

Bu görev, garanti mektubu işlemek için gereken banka tesisi ve deftere nakil profilini oluşturur.



Bu görevde USMF demo şirketi kullanılmaktadır. 




## <a name="general-ledger-parameter"></a>Genel muhasebe defteri parametresi
1. Nakit ve Banka yönetimi > Kurulum > Nakit ve Banka yönetim parametreleri.
2. Banka belgesi bölümünü genişletin.
3. Teminat mektubunu etkinleştirme seçeneğini seçin.
4. Dönüştürme günlüğü alanında, aramayı açmak için açılır menü düğmesine tıklayın.
5. Listede, istenen kaydı bulun ve seçin.
6. Listede, seçili satırdaki bağlantıya tıklayın.
7. Numara serileri sekmesini tıklatın.
    * Teminat mektubu numarası ve teminat mektubu hareket referansı için sayı sıra numarası kodunu tanımlayın.  
8. Kaydet'e tıklayın.
9. Sayfayı kapatın.

## <a name="create-bank-facility"></a>Banka hizmeti yarat
1. Nakit ve Banka yönetimi > Kurulum > Banka tesisleri seçeneğine gidin.
2. Yeni'ye tıklayın.
3. Tesis grubu alanına, teminat mektubu hareketi için banka tesisi grup adını girin.
4. Açıklama alanına bir değer girin.
5. Kaydet'e tıklayın.
6. Tesis türleri sekmesini tıklatın.
7. Yeni'ye tıklayın.
8. Tesis türü alanında, banka tesisi anlaşmasıyla ilişkili banka tesisi türünün adını girin.
9. Tanım alanına bir değer girin.
10. Tesis grubu alanında, aramayı açmak için açılır menü düğmesine tıklayın.
11. Listede, istenen kaydı bulun ve seçin.
12. Listede, seçili satırdaki bağlantıya tıklayın.
13. Tesis niteliği alanında, bir seçenek seçin.
14. Kaydet'e tıklayın.
15. Sayfayı kapatın.

## <a name="bank-posting-profile"></a>Banka nakil profili
1. Nakit ve Banka yönetimi > Kurulum > Banka belgesi nakletme profili seçeneğine gidin.
2. Yeni'ye tıklayın.
3. Hesap/Grup numarası alanında, aramayı açmak için açılır menü düğmesini tıklatın.
4. Listede, istenen kaydı bulun ve seçin.
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. Hesabı kapatma alanında, hesap kapatma için ana hesabı seçin.
7. Gider hesabı alanında masraf hareketleri hesabını seçin.
8. Marj hesabı alanında, marj hareketi hesabını seçin.
9. Tasfiye hesabı alanında, teminat mektubu hareketi için tasfiye hesabını seçin. 
10. Kaydet'i tıklatın.
11. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]