---
title: Açık uçlu devamsızlık izni oluşturma
description: Bu makalede, Microsoft  Dynamics 365 Human Resources'ta açık uçlu devamsızlık kaydının nasıl oluşturulacağı açıklanır.
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 08231d4139209387c3c76923fafdd2061fceb280
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805350"
---
# <a name="create-an-open-ended-leave-of-absence"></a>Açık uçlu devamsızlık izni oluşturma

> [!IMPORTANT]
> Bu makalede açıklanan işlev, Microsoft Dynamics 365 Finance 10.0.31 sürümünden sonra Finance altyapısında ileride yayınlanacak bir sürümünün parçası olarak kullanılacaktır.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Açık uçlu bir devamsızlık durumu için istek gönderebilir ve Dynamics 365 Human Resources'ta izin taleplerinizin durumunu görebilirsiniz.

## <a name="prerequisites"></a>Ön Koşullar

1. **Özellik yönetimi**  altında **Açık uçlu izin**  özelliğinin açık olduğundan emin olun.

    > [!IMPORTANT]
    > Bu özellik, açıldıktan sonra kapatılamaz.

2. Bir devamsızlık izin türü oluşturun.
3. İzin türü, açıklama ve iş akışı kodu gibi ayrıntıları girin.
4. **İstek türü** alanında **Devamsızlık** seçeneğini belirtin.
5. Ayrıntılar bölümünde, açık uçlu izinler için **Açık Uçlu** seçeneğini **Evet** olarak ayarlayın.
6. **İşe dönüş bildirimi** seçeneğini **Evet** veya **Hayır** olarak ayarlayın.
7. Açık uçlu devamsızlık istekleri için isteğe bağlı olarak br işe dönüş bildirimi gerekli olabilir.

> [!NOTE]
> Bu özellik etkinleştirildikten sonra **Ek gerekli** özelliği etkinleştirilir.

## <a name="request-an-open-ended-leave-of-absence"></a>Açık uçlu devamsızlık izni isteme

1. **Personel Self servis** çalışma alanında, **İzin bakiyesi** kutucuğunda **Diğer (...)** seçeneğini seçin.
2. Devamsızlık talebi bırak göndermek için **Devamsızlık izni iste** seçeneğini belirleyin.
3. **İzin türü** ve **Başlangıç tarihi** alanlarına bilgi girin. **Bitiş tarihi** alanına tahmini bir bitiş tarihi girin.
4. Herhangi bir destekleyen belgeyi göndermeniz gerekiyorsa, **Ekler**'in altında **Yükle**'yi seçin.
5. İsteğinizi göndermeye hazır olduğunuzda **Gönder**'i seçin. Aksi durumda, **Taslağı kaydet**'i seçin.
6. Açık uçlu bir izin isteğini güncelleştirmek için isteği seçin, **Bitiş tarihi** alanına bir bitiş tarihi girin, **Bitiş tarihini onayla** seçeneğini **Evet** olarak ayarlayın ve belgeleri karşıya yükleyin.
7. **İşe dönüş bildirimi** seçeneği **Evet** olarak ayarlanmışsa, **Yükle**'yi seçin ve sonra geçerli işe dönüş bildiriminin karşıya yüklendiğini onaylamak için onay kutusunu seçin.
8. Tüm ayrıntılar girildiğinde **Gönder**'i seçin.
