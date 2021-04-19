---
title: Ambar işiyle ilgili sorunları giderme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta ambar işiyle çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 08cc074fe851b952ebfc942ae3d1cb05240d3b91
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837453"
---
# <a name="troubleshoot-warehouse-work"></a>Ambar işiyle ilgili sorunları giderme

[!include [banner](../includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta ambar işiyle çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a>İzleme boyut grubunda boş çıkış ve boş girişe izin verildiğinde, seri numarası maddeleri olan plakaları taşıyamıyorum.

### <a name="issue-description"></a>Sorun açıklaması

İzleme boyutu grubunda, seri numarasında *Boş çıkışa izin verilir* ve *Boş girişe izin verilir* ayarları varsa ve aynı konumda bazılarında seri numarası olan ve bazılarında olmayan birden fazla plaka varsa **Hareket** menüsü öğesini kullanarak bir plakaları taşıyamazsınız.

### <a name="issue-resolution"></a>Sorunun çözümü

Bu sorun [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687)'da dağıtılan değişikliklerle düzeltilecektir. Boş girişe ve boş çıkışa izin verildiğinde, bu değişiklikler **Seri numarası** alanını isteğe bağlı yapar.

## <a name="i-receive-the-following-error-message-in-the-warehouse-management-mobile-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a>Hareketleri işlediğimde Ambar Yönetimi mobil uygulamasında aşağıdaki hata iletisini alıyorum: "Bu işlemde %1 adlı stok sahibine izin verilmiyor."

### <a name="issue-description"></a>Sorun açıklaması

Ambar Yönetimi mobil uygulaması, hareketleri oluşturmak için kullanıldığında **Sahip** izleme boyutu eksiktir. Supply Chain Management istemcisinden alınan düzenli bir stok transferi günlüğü, istendiği gibi çalışır ve yalnızca **Sahip** boyutu doldurulmuşsa deftere nakledilebilir.

### <a name="issue-resolution"></a>Sorunun çözümü

Microsoft bu sorunu değerlendirmiş ve bir özellik sınırlaması olduğunu tespit etmiştir. Şu anda, ambar yönetimi işlemleri yalnızca tüzel kişiliklerin sahip olduğu stokları destekler.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]