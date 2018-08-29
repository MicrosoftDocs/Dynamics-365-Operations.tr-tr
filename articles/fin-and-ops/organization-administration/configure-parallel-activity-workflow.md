---
title: "İş akışında paralel etkinlikleri yapılandırma"
description: "Paralel faaliyet yapılandırmak için iş akışı düzenleyicisinde aşağıdaki yordamları tamamlayın."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 64cd387f8a6ab693d159cd659fca51fa6568ee39
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---

# <a name="configure-parallel-activities-in-a-workflow"></a>İş akışında paralel etkinlikleri yapılandırma

[!include [banner](../includes/banner.md)]

Paralel faaliyet yapılandırmak için iş akışı düzenleyicisinde aşağıdaki yordamları tamamlayın.

Paralel faaliyet aynı anda çalışan iş akışı dallarından oluşur.

## <a name="name-a-parallel-activity"></a>Paralel faaliyete ad verme
Paralel faaliyete bir ad vermek için aşağıdaki adımları uygulayın.
1.  Paralel faaliyete sağ tıklayın ve ardından **Özellikler** formunu açmak için **Özellikler**'e tıklayın.
2.  Sol bölmede **Temel Ayarlar**'a tıklayın.
3.  Paralel faaliyet için **Ad** alanına benzersiz bir ad girin.
4.  **Kapat**'a tıklayın.

## <a name="configure-the-branches-of-a-parallel-activity"></a>Paralel faaliyetin dallarını yapılandırma
Bu paralel faaliyete dal eklemek ve paralel faaliyetin dallarını yapılandırmak için bu adımları izleyin.
1. Paralel faaliyetin dallarını görüntülemek için paralel faaliyete çift tıklayın.
2. Dal eklemek için **İş akışı öğeleri** alanından **Dal** öğesini tuval üzerinde bir ekleme noktasına sürükleyin. Aşağıdaki şekil bir ekleme noktasını gösterir.![Ekleme noktası](./media/workflow_insertionpoint.gif)

   |                                              <strong>Not</strong>                                               |
   |------------------------------------------------------------------------------------------------------------------|
   | Paralel faaliyetin tüm dalları aynı anda çalıştığından dalların sırası önemli değildir. |


3. Her bir dalı yapılandırmak için bkz. [Paralel dal yapılandırma](configure-parallel-branch-workflow.md).






