---
title: Toplu iş oluşturma
description: Toplu iş, otomatik işlem için bir Uygulama Nesne Sunucusu (AOS) kurulumuna gönderilmiş görevlerin bir grubudur.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4360cd7068658a170f5b44c2ce7c71c39c44fa8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679900"
---
# <a name="create-a-batch-job"></a>Toplu iş oluşturma

[!include [banner](../../includes/banner.md)]

Toplu iş, otomatik işlem için bir Uygulama Nesne Sunucusu (AOS) kurulumuna gönderilmiş görevlerin bir grubudur. Toplu işler işi oluşturan kullanıcının güvenlik kimlik bilgilerini kullanarak çalışır. Toplu bir iş oluşturmak için aşağıdaki yordamı kullanın. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="create-the-batch-job"></a>Toplu işi oluşturun
1. **Gezinti bölmesi > Modüller > Sistem yönetimi > Sorgular > Toplu işler**'e gidin.
2. **Yeni**'ye tıklayın.
3. **İş açıklaması** alanına bir değer yazın.
4. **Planlanan başlangıç tarihi/saati** alanına bir tarih ve saat girin.
5. **Kaydet**'e tıklayın.

## <a name="create-a-recurrence"></a>Yineleme oluşturun
1. Eylem Bölmesi'nde **Toplu iş**'e tıklayın.
2. **Yineleme**'ye tıklayın. Bu seçenekleri bir aralık ve yineleme için model girmek için kullanın.  
3. **Tamam**'a tıklayın.

## <a name="add-alerts"></a>Uyarılar ekleyin
1. Eylem Bölmesi'nde **Toplu iş**'e tıklayın.
2. **Uyarılar**'a tıklayın. Toplu işlem bittiğinde, bir hata olduğunda veya iptal edildiğinde uyarı iletileri istiyorsanız belirtin. Ardından uyarıların açılır pencere iletileri olarak gösterilmesini istiyorsanız belirtin.   
3. **Tamam**'a tıklayın.

## <a name="adjust-batch-job-status"></a>Toplu iş durumunu düzelt
1. **Sistem yönetimi > Sorgular > Toplu işler**'e gidin.
2. Uygun olan toplu işi seçin.
3. Eylem Bölmesi'nde **Toplu iş > İşlevler > Durumu değiştir**'e tıklayın.
4. Uygun olan durumu seçin:
    - **Stopaj**: Toplu işi **stopaj** olarak ayarlayın, böylece toplu iş planlayıcısından kesilir. *Durdur* ile eşdeğerdir.
    - **Bekliyor**: Toplu işi **bekliyor** olarak ayarlayın, böylece toplu iş planlayıcısı tarafından alınmayı bekler. *Git* ile eşdeğerdir.
5. **Tamam**'a tıklayın.
