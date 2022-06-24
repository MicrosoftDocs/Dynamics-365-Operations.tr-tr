---
title: Uluslararası Banka Hesap Numarası (IBAN) hesap doğrulamasını yönetme
description: Bu makalede, Uluslararası Banka Hesap Numarası (IBAN) hesap doğrulamasını yönetme işlemi açıklanmaktadır.
author: twheeloc
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 3d825e8699fbe10e080cd85f15d3d86f8c780f15
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880913"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a>Uluslararası Banka Hesap Numarası (IBAN) hesap doğrulamasını yönetme

[!include [banner](../includes/banner.md)]

Uluslararası Banka Hesap Numarası (IBAN) doğrulaması bir banka hesabına IBAN eklediğinizde gerçekleştirilen doğrulamanın miktarını artırır.

IBAN yapısıyla ilgili bilgiler Microsoft Dynamics 365 Finance'te depolanır ve IBAN'ı banka hesaplarında ilk kez kullandığınızda otomatik olarak yüklenir. IBAN uzunluğu, banka hesap numarasının başlangıç konun ve rota numarası, banka hesap numarası uzunluğu ve rota numarasını içerir.

## <a name="set-up-iban-structures"></a>IBAN yapılarını ayarlama

1. **Nakit ve banka yönetimi \> Kurulum \> IBAN yapıları** seçeneğine gidin.
2. Her ülkenin veya bölgenin IBAN yapılarının otomatik olarak ayarlandığına dikkat edin.
3. Yapının belirli bir ülke veya bölge için güncelleştirilmesi gerekiyorsa **Düzenle** düğmesini seçin.
4. Yapı tanımları her yeni sürümün parçası olarak sunulur. **Yapıları sıfırla** menüsünü her güncelleştirmeden sonra en son tanımları yüklemek için kullanabilirsiniz.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>Banka hesabındaki IBAN yapısını doğrulama

1. **Nakit ve banka yönetimi \> Banka hesapları \> Banka hesapları** öğesine gidin.
2. Banka hesabı oluşturun.
3. **Ek bilgiler** hızlı sekmesinde bir IBAN girin.

    Her ülke veya bölge için tanımlanan uzunlukla IBAN'ın uzunluğu eşleşmiyorsa, bir uyarı iletisi alacaksınız. IBAN'ın uzunluğu IBAN yapısında belirtilen uzunlukla eşleşmezse işleme devam edemezsiniz.

    Doğrulama, banka hesap numarasının IBAN'ın banka hesap numarasını temsil eden kısmıyla eşleştiğini de doğrular. Banka hesap numarası eşleşmiyorsa bir uyarı iletisi alırsınız. Bir ileti yalnızca bir uyarıdır. Banka hesap numarası eşleşmese de işleme devam edebilirsiniz.

    Doğrulama, banka rota numarasının IBAN'ın banka rota numarasını temsil eden kısmıyla eşleştiğini de doğrular. Rota numarası, banka numarası ve genellikle bir ek banka şubesi içerir. Banka rota numarası eşleşmiyorsa bir uyarı iletisi alırsınız. Bir ileti yalnızca bir uyarıdır. Banka rota numarası eşleşmese de işleme devam edebilirsiniz.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
