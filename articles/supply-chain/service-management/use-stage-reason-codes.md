---
title: Aşama neden kodlarını kullanma
description: Bir servis düzeyi sözleşmesinin (SLA) neden iptal edildiğini veya bir servis siparişinin SLA'da tanımlanan süre limitini neden aştığını belirtmek için bir neden kodu kullanırsınız.
author: sorenva
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06c2b6a2b338dbfdbecdeb75e12fa1c20af8e56d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669530"
---
# <a name="use-stage-reason-codes"></a>Aşama neden kodlarını kullanma 

[!include [banner](../includes/banner.md)]


Bir servis düzeyi sözleşmesinin (SLA) neden iptal edildiğini veya bir servis siparişinin SLA'da tanımlanan süre limitini neden aştığını belirtmek için bir neden kodu kullanırsınız.

Ayrıca SLA iptal edildiğinde veya süre limiti servis siparişi için SLA'da belirtilen süreyi aştığında bir neden kodunun gerekli olduğunu belirtebilirsiniz.

Neden kodunun gerekli olduğunu belirttiyseniz, aşağıdaki durumlarda bir neden kodu girmeniz gerekir:

  - Servis siparişi, servis siparişine yönelik SLA'ya karşı zaman kaydını durduran bir aşamaya geldiğinde.

  - Servis siparişi imzalandığında.

  - Zaman kaydı el ile durdurulduğunda.

## <a name="set-up-reason-codes"></a>Neden kodlarını ayarla

1.  **Servis yönetimi** \> **Kurulum** \> **Servis siparişleri** \> **Aşama neden kodları**'na tıklayın.

2.  **Aşama neden kodları** formunda, **Yeni**'ye tıklayarak yeni bir neden kodu oluşturun.

3.  **Aşama neden kodu** alanına, benzersiz bir aşama neden kodu girin.

4.  **Açıklama** alanına, aşama neden kodu açıklaması girin.

5.  Değişikliklerinizi kaydetmek için formu kapatın.

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a>Bir servis düzeyi anlaşması iptal edildiğinde neden kodu gerektirme

1.  **Servis yönetimi** \> **Kurulum** \> **Servis yönetimi parametreleri**'ne tıklayın.

2.  **Servis yönetimi parametreleri** formunda, **Genel** bağlantısına tıklayın ve sonra **İptal durumunda neden kodu** onay kutusunu işaretleyin.

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a>Servis siparişi, servis düzeyi sözleşmesi tarafından ayarlanan süre limitini aştığından neden kodu gerektir

1.  **Servis yönetimi** \> **Kurulum** \> **Servis yönetimi parametreleri**'ne tıklayın.

2.  **Servis yönetimi parametreleri** formunda, **Genel** bağlantısına tıklayın ve sonra **Süre aşımında neden kodu** onay kutusunu işaretleyin.

## <a name="see-also"></a>Ayrıca bkz.

[Servis siparişinde zaman kaydını başlatma ve durdurma](start-and-stop-time-recording-on-a-service-order.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]