---
title: Test sırasında istek ile oturum verileri arasında beklenmeyen fark oluştu
description: Ambar uygulama görevi doğrulama sonuçlarındaki istek ve oturum verileri arasında beklenmeyen bir fark oluşur.
author: mamuszal
ms.date: 03/11/2022
ms.topic: troubleshooting
ms.search.form: WHSValidatorRunInstance_executeRun
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mamuszal
ms.search.validFrom: 2022-03-11
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: da8f0506a76b0d0cc02bfc2e1bff01b4ddccb578
ms.sourcegitcommit: 941119133be1765f653d5d5270dfdf58466e1d07
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/17/2022
ms.locfileid: "8456949"
---
# <a name="unexpected-difference-between-request-and-session-data-during-testing"></a>Test sırasında istek ile oturum verileri arasında beklenmeyen fark oluştu

Hata kodu: WarehouseMobileDeviceRequestInputValidationError

## <a name="symptoms"></a>Belirtiler

[Ambar uygulaması görev doğrulama çerçevesini](/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/warehouse-app-task-validation-rsat) kullanırken, doğrulayıcı aşağıdaki hata iletisini döndürür:

> İstek ile oturum verileri arasında beklenmeyen fark oluştu. Warehouse Mobile Devices XML protokol ihlali.REQUEST_XML_TAMPERING

## <a name="cause"></a>Nedeni

Hata, test çalıştırmasında başarıyla çalıştırılan son adımın çıktısı bir sonraki adım için kaydedilen girişle eşleşmezse oluşur. Bu durum, görev doğrulayıcı önceki adımdaki çıktıyı art arda bir adım için giriş olarak kullanmadan ortaya çıkabilir. Bunun yerine, her adım için giriş olarak kaydedilen XML'yi kullanır.

Çoğu durumda, bir görevi yeniden çalıştırdığınızda ancak testin, aynı görevin önceki çalıştırmalarında değiştirilen veya kaldırılan bazı kayıtları gerektirdiği durumlarda bu hata oluşur.

## <a name="resolution"></a>Çözüm

Ambar uygulama görevi doğrulama test çalıştırması bir etkili olacak işlem değildir ancak temel alınan verileri değiştiriyor. Bu nedenle, bir görevi yeniden çalıştırmadan önce ilgili verileri sıfırlamanız gerekebilir.

1. Test çalıştırmasının nerede bırakıldığını belirlemek için, son başarılı test adımının çıktı XML'sini gözden geçirin.
1. Testinizi inceleyin ve gerekli tüm satış siparişlerinin, transfer emirlerinin, iş başlıklarının ve diğer kayıtların hala mevcut olduğundan ve beklenen durumda olduğundan emin olun.
1. Eksik veya değiştirilmiş kayıtları yeniden oluşturun veya düzenleyin. Alternatif olarak, yeni bir test kurulumu oluşturabilir ve geçerli varolan kayıtları kullanacak şekilde testi tasarlayabilirsiniz.
