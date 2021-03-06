---
title: Gelişmiş ambar yönetimine yükseltme ve geçiş ile ilgili sorunları giderme
description: Bu konuda, gelişmiş ambar yönetimine yükseltme ve geçiş sırasında karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmaktadır.
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
ms.openlocfilehash: 12dcadae2a65d71614a2eee9468ec93cac284a7b
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907899"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a>Gelişmiş ambar yönetimine yükseltme ve geçiş ile ilgili sorunları giderme

[!include [banner](../includes/banner.md)]

Bu konuda, gelişmiş ambar yönetimine yükseltme ve geçiş sırasında karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmaktadır.

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a>Şu hata iletisini alıyorum: "java.security.cert.certPathValidatorException: Sertifika yolu için güven çıpası bulunamadı."

### <a name="issue-description"></a>Sorun açıklaması

Bu hata iletisini Ambar Yönetimi mobil uygulamasında alırsınız çünkü otomatik olarak imzalanan sertifikalara şirket içi ortamlarda Android 8+ sistemlerde güvenilmez.

### <a name="issue-resolution"></a>Sorunun çözümü

Harici (ortak) bir sertifika yetkilisi (CA) kullanın. Bu sorunla ilgili düzeltme, ambar uygulamasının 1.9.0.0 sürümünde kullanıma sunulmuştur. Bu sorun ve nasıl düzeltileceği hakkında daha fazla bilgi için bkz. [Ambar Yönetimi mobil uygulaması bağlantı sorunlarını giderme](troubleshoot-warehouse-app-connection.md).

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a>Temel ambar işlemlerinden gelişmiş ambar işlemlerine geçiş için onaylı işlem nedir?

### <a name="issue-description"></a>Sorun açıklaması

Şu anda envanter/stok yönetimi altında çalıştırıyor ve temel stok işlevlerini kullanıyorsunuz ve mobil cihazlardan, dalgalardan ve işlerden yararlanmak için Gelişmiş ambar işlemlerine geçmek istiyorsunuz. Ancak, bu taşımayı yapmaya çalıştığınızda sorunlarla karşılaşabilirsiniz. Örneğin, ürünleri depolama boyutları (tesis, ambar ve konum) kullanacak şekilde değiştiremezsiniz çünkü ürünlerin kendilerine karşı hareketler vardır. Bu nedenle, temel ambar işlemlerinden gelişmiş ambar işlemlerine geçiş için onaylı işlemi öğrenmeniz gerekir.

### <a name="issue-resolution"></a>Sorunun çözümü

Temel ambar işlemlerinden gelişmiş ambar işlemlerine geçiş hakkında daha fazla bilgi için aşağıdaki blog gönderilerine ve belgelere bakın:

- [Mevcut maddeler ve ambarlar için ambar yönetimi işlemini etkinleştirme](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [Microsoft Dynamics AX WMS'den yeni R3 ambar ve taşımacılık işlevine geçiş](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [WMSI/WMS2 madde geçişi](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [Ambar yönetimini Microsoft Dynamics AX 2012'den Supply Chain Management'a yükseltme](./upgrade-migration-warehouse-management-processes.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]