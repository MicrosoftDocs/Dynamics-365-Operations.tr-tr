---
title: "Bir iş akışında bir paralel etkinlik yapılandırma"
description: "Paralel faaliyet yapılandırmak için iş akışı düzenleyicisinde aşağıdaki yordamları tamamlayın."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: ce3fca9d2dbca046232365b1375bfd920d5b10fd
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="configure-a-parallel-activity-in-a-workflow"></a>Bir iş akışında bir paralel etkinlik yapılandırma

[!include[banner](../includes/banner.md)]


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
1.  Paralel faaliyetin dallarını görüntülemek için paralel faaliyete çift tıklayın.
2.  Dal eklemek için **İş akışı öğeleri** alanından **Dal** öğesini tuval üzerinde bir ekleme noktasına sürükleyin. Aşağıdaki şekil bir ekleme noktasını gösterir.![Ekleme noktası](./media/workflow_insertionpoint.gif)
    | **Not**                                                                                                         |
    |------------------------------------------------------------------------------------------------------------------|
    | Paralel faaliyetin tüm dalları aynı anda çalıştığından dalların sırası önemli değildir. |

3.  Her bir dalı yapılandırmak için bkz. [Paralel dal yapılandırma](configure-parallel-branch-workflow.md).






