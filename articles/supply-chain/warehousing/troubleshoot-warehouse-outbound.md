---
title: Giden ambar işlemlerinde sorun giderme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta giden ambar işlemleriyle çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 165ac8145ad75c2c6619764b9abe855b9d32eb46
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993990"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a>Giden ambar işlemlerinde sorun giderme

[!include [banner](../includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta giden ambar işlemleriyle çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a>Şu hata iletisini alıyorum: "Satış siparişi serbest bırakılamadı."

### <a name="issue-description"></a>Sorun açıklaması

Bu sorun birkaç nedenle oluşabilir. Örneğin, sipariş alacak yönetimi tutuluyor durumundadır ve bir satış siparişiyle ilişkili tüm satış satırları için geçerli bir posta adresi girilene kadar hiçbir sevkiyat oluşturulamaz. Alternatif olarak, siparişin ambara serbest bırakılması için önce giderilmesi gereken bir sipariş tutma işlemi vardır. Bu tutma işlemi, siparişe özgü olabilir veya müşteri hesabı üzerinde olabilir.

### <a name="issue-resolution"></a>Sorunun çözümü

Satış siparişi ve sipariş satırlarına adres ekleyin veya adresi güncelleştirin, ardından siparişi ambara serbest bırakın. Siparişler yalnızca geçerli teslimat adresi varsa (**Kuruluş yönetimi** modülünde ayarlanan adres biçimi kurulumu için) ambara serbest bırakılabilir.

Sipariş tutmayı araştırın ve sorunları giderin. Ardından sipariş veya müşteriden tutma işlemini kaldırın ve siparişi ambara serbest bırakın.

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a>Şu iletiyi alıyorum: "%1 yükü için sevkiyat onaylandı." Ancak hiçbir satır deftere nakledilmiyor.

### <a name="issue-description"></a>Sorun açıklaması

Bir yükle ilgili sevkiyat onaylanmıştır ancak başka bir deftere nakil işlemi gerçekleşmemiştir.

### <a name="issue-resolution"></a>Sorunun çözümü

Sevkiyat onayı deftere nakli etkilemez. Yalnızca sevkiyat ve yük durumunu güncelleştirir. Deftere nakletme işlemi ayrı bir işlemde olmalıdır.

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a>Şu hata iletisini alıyorum: "Ambar yönetimi etkinleştirilmiş olduğundan, doğrudan teslimat %1 ambarı için işlenemiyor. Lütfen ambar yönetimi için etkinleştirilmemiş olan başka bir ambar belirtin."

### <a name="issue-description"></a>Sorun açıklaması

Ambar yönetimi (WMS) için etkinleştirilmiş bir ambardan doğrudan teslimatın satış satırına bir madde eklenir. Satış satırı güncelleştirildiğinde bu hata iletisini alırsınız. 

### <a name="issue-resolution"></a>Sorunun çözümü

Microsoft bu sorunu değerlendirmiş ve bir özellik sınırlaması olduğunu tespit etmiştir. Şu anda WMS doğrudan teslimi desteklemiyor. Bu nedenle, doğrudan teslimi kullanmak için WMS harici bir madde ve ambar seçmelisiniz.
