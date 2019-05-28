---
title: Çekme kanbanı kuralı oluşturma
description: Bu prosedürde, yalın bir ortamda malzeme aktarılması için bir çekme kanban kuralının oluşturulmasında gerekli kurulum açıklanmıştır.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a77c66b64512274f2703543293c2f48f2df2acf5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570164"
---
# <a name="create-a-withdrawal-kanban-rule"></a>Çekme kanbanı kuralı oluşturma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu prosedürde, yalın bir ortamda malzeme aktarılması için bir çekme kanban kuralının oluşturulmasında gerekli kurulum açıklanmıştır. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu prosedür, yeni veya değiştirilmiş bir malzemenin stokta yenilenmesi için hazırlık yaparken İşlem Mühendisinin veya Değer Akışı Yöneticisinin yararlanması için hazırlanmıştır.


## <a name="create-new-kanban-rule"></a>Yeni kanban kuralı oluştur
1. Kanban kuralları'na gidin.
2. Yeni'ye tıklayın.
3. Tür alanından 'Çek' seçimini yapın.
    * Çekme türü, malzemelerin veya malların transfer edilmesi için kanban kurallarına yönelik kullanılır.  
4. İlk plan alanında bir değer girin veya bir değer seçin.
    * ReplenishSpeakerComponents öğesini seçin.   Bu etkinlik, bileşenleri ambar 11'den ve konum 11'den ambar 12'ye ve konum 12'ye taşıyacak şekilde ayarlanır.  
5. Ürün alanında bir değer girin veya bir değer seçin.
    * M0007 öğesini seçin.  
6. Sağlama süresi alanında bir sayı girin.
    * Örneğin, 60.  
7. Ölçü birimi alanında bir değer girin veya bir değer seçin.
    * Örneğin, Dakikalar.  

## <a name="set-quantities-for-kanban"></a>Kanban için miktarları ayarlama
1. Varsayılan mktarı '5' olacak şekilde ayarlayın.
    * Bu, her kanban için transfer edilecek miktardır.  
2. Sabit kanban miktarı alanına '2' girin.
    * Bu, kanbanların etkin olması gereken tutardır. Bu durumda, her 5 tane için 2 kanban aktarılır.  
3. Uyarı sınırı minimumı alanında '1' girin.
    * Hedefte olması gereken tam kanbanların minimum tutarını izlemek için kullanılır. Örneğin, bu kanban tutarının genel görünümüne ilişkin kullanılır.  
4. Uyarı sınırı maksimumu alanında '2' girin.
    * Hedefte olması gereken tam kanbanların maksimum tutarını izlemek için kullanılır. Örneğin, bu kanban tutarının genel görünümüne ilişkin kullanılır.  

## <a name="create-kanbans"></a>Kanban oluştur
1. Kaydet'e tıklayın.
    * Kanbanlar oluşturulmadan önce kanban kuralının kaydedilmesi gerekir.  
2. Ekle öğesini tıklatın.
    * Önerilen kanban 'Yeni kanban sayısı' 2 olduğundan hiçbir etkin kanban olmadığını unutmayın. Bu, 'Sabit kanban tutarı' ile eşittir.  
3. Oluştur'a tıklayın.
    * Bu da iki kanban oluşturur.  
    * Bu çekme kanbanı kuralı için her 5 başına 2 kanban oluşturulduğunu unutmayın.  Bu yordamın son aşamasıdır.  

