--- 
title: "El ile navlun mutabakatı sağlama"
description: "Bu yordam navlunun el ile nasıl mutabık kılınacağını gösterir."
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 28de4c720cd771f476f379d925e9500e41482aa6
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="reconcile-freight-manually"></a>El ile navlun mutabakatı sağlama

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu yordam navlunun el ile nasıl mutabık kılınacağını gösterir. Bu genellikle taşımacılık düzenleyicisi tarafından yapılır. Bu yordamı USMF demo veri şirketinde kullanabilirsiniz.


## <a name="select-a-load-to-reconcile"></a>Mutabık kılınacak yükü seçme
1. Taşıma yönetimi > Planlama > Yük planlama çalışma ekranına gidin.
2. Sevk edileni ve teslim alınanı gizle onay kutusunu temizleyin. 
3. Listede yük kimliği 00006 olan yükü seçin.

## <a name="create-a-carrier-invoice"></a>Taşıyıcı faturası oluşturma
    * Navlunu el ile mutabık kılarsanız ve taşıyıcı faturasını otomatik olarak almazsanız navlun faturasına göre bir fatura oluşturabilirsiniz.  
1. İlgili bilgiler'e tıklayın.
2. Navlun faturası ayrıntıları'na tıklayın.
3. Navlun faturası oluştur'a tıklayın.
4. Fatura alanına bir değer girin.
5. Tamam'a tıklayın.

## <a name="reconcile-the-invoice"></a>Fatura için mutabakat sağlama
    * Taşıyıcı faturasını ve navlun faturasını mutabık kıldığınızda bu işlem satır satır yapılır.  
1. Navlun faturaları ile faturaları eşleştir'e tıklayın.
2. Fatura ayrıntıları bölümünü genişletin.
3. Eşleştirilmeyen navlun fatura ayrıntıları bölümünü genişletin.
4. Listede, seçili satırı işaretleyin.
5. Eşleştir'e tıklayın.
6. Eşleştirilen navlun faturası ayrıntıları bölümünü genişletin.

## <a name="submit-the-invoice-for-approval"></a>Faturayı onay için gönder
1. Onay için gönder'e tıklayın.
2. Sayfayı kapatın.
3. Onaylananı gizle onay kutusunu temizleyin. 
4. Satıcı fatura günlükleri'ne tıklayın.
5. Referans günlük numarası alanındaki bağlantıyı izlemek için tıklayın.
6. Satırlar seçeneğine tıklayın.


