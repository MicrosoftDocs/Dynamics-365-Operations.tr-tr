---
title: Zaman uyumsuz müşterileri zaman uyumlu müşterilere dönüştürme
description: Bu makale, zaman uyumsuz müşterilerin Microsoft Dynamics 365 Commerce'te zaman uyumlu müşterilere nasıl dönüştürüleceğini açıklamaktadır.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 0ce4906816deab8824b1079a34489e55651c0e03
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884403"
---
# <a name="convert-asynchronous-customers-to-synchronous-customers"></a>Zaman uyumsuz müşterileri zaman uyumlu müşterilere dönüştürme

[!include [banner](includes/banner.md)]

Bu makale, zaman uyumsuz müşterilerin Microsoft Dynamics 365 Commerce'te zaman uyumlu müşterilere nasıl dönüştürüleceğini açıklamaktadır.

Zaman uyumsuz müşterileri zaman uyumlu müşterilere dönüştürmek için bu adımları izleyin.

1. Commerce Headquarters'da zaman uyumsuz müşterileri Commerce Headquarters'a göndermek için **P İşi**'ni çalıştırın.
1. Müşteri hesap kodları oluşturmak için **müşterileri ve iş ortaklarını zaman uyumsuz modda Eşitle** işini çalıştırın. (Bu iş daha önce **Müşterileri ve iş ortaklarını zaman uyumsuz moddan eşitleme** olarak adlandırılıyor.)
1. Yeni müşteri hesap kodlarını kanallarla eşitlemek için **1010** işini çalıştırın.

Sipariş henüz Commerce Headquarters ile eşitlenmemiş bir zaman uyumsuz bir müşteriye veya adrese başvuruyorsa müşteri veya adres, **Siparişleri eşitle** toplu işleminin bir parçası olarak eşitlenir. Bir nakit ve taşıma hareketi zaman uyumsuz bir müşteri veya adrese başvuruyorsa müşteri veya adres, gün sonunda (EOD) deftere nakledilmeden önce eşitlenir.

## <a name="additional-resources"></a>Ek kaynaklar

[Mağazalardaki müşteri yönetimi](customer-mgmt-stores.md)

[Zaman uyumsuz müşteri oluşturma modu](async-customer-mode.md)

[Müşteri öznitelikleri](dev-itpro/customer-attributes.md)

[Çevrimdışı veri hariç tutma](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
