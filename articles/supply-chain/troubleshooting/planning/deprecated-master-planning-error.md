---
title: Yerleşik master planlama altyapısını çalıştırırken bir hata alıyorsunuz
description: Kullanım dışı bırakılan yerleşik master planlama altyapısını çalıştırdığınızda bir hata iletisi alıyorsunuz.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: Dialog_ReqCalcScheduleItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c950292a4f43319d21a7deafdfb341b7bef15d8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294201"
---
# <a name="you-receive-an-error-when-running-the-built-in-master-planning-engine"></a>Yerleşik master planlama altyapısını çalıştırırken bir hata alıyorsunuz

Hata kodu: ReqCalcScheduleItemTablePlanningOptimizationFitError

## <a name="symptoms"></a>Belirtiler

Master planlamayı kullanım dışı bırakılan yerleşik master planlama altyapısını kullanarak çalıştırdığınızda aşağıdaki hata iletisini alırsınız:

> Bu hata iletisini, yerleşik master planlama altyapısı Planlama İyileştirmesi tarafından desteklenen senaryolar için kullanıldığı için alırsınız. Geçerli yerleşik master planlama kullanım dışı bırakılacağından şimdi Planlama İyileştirmesi'ne geçiş yapmalısınız. Bu master planlama çalıştırmasının başarıyla tamamladığını unutmayın. Geçişinizin beklemedeki özelliklere güçlü bağımlılıkları olması durumunda, yerleşik master planlama altyapısının sürekli kullanımı için bir özel durum isteyebilirsiniz. Başlamak için lütfen aşağıdaki anketi doldurun ve ilgili istek durumunda Planlamayı En İyi Duruma Getirme'ye geçişle ilgili özel bir durum isteyin. [Planlamayı En İyi Duruma Getirme geçişi ve özel durum anketi](https://go.microsoft.com/fwlink/?linkid=2144962)

## <a name="cause"></a>Nedeni

Planlamayı çalıştırırsanız ve üretim denetimi özelliklerini kullanmıyorsanız, Planlamayı En İyi Duruma Getirme'ye geçiş yapmayı düşünmelisiniz. Yerleşik master planlama altyapısı kullanımdan kaldırılıyor. Bu nedenle, hata iletisi almadan kullanmaya devam etmek istiyorsanız, Microsoft'a bir özel durum başvurusunda bulunmalısınız.

## <a name="resolution"></a>Çözüm

Planlamayı En İyi Duruma Getirme'ye geçiş yapma veya bunun yerine kullanımdan kaldırılan yerleşik planlama altyapısını kullanmaya devam edebilmeniz için özel durum başvurusu yapma hakkında daha fazla bilgi için bkz. [Master planlama için Planlamayı En İyi Duruma Getirmeye Geçiş](/dynamics365/supply-chain/master-planning/new-master-planning-engine).
