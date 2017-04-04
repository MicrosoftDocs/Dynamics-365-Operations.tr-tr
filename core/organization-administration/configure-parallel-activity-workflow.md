---
title: "Paralel bir etkinlik içinde bir iş akışı yapılandırma"
description: "Paralel faaliyet yapılandırmak için iş akışı düzenleyicisinde aşağıdaki yordamları tamamlayın."
author: sericks007
manager: AnnBe
ms.date: 2017-04-04
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
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 818fb054742b935d002a7341e54a37eca0bb4761
ms.lasthandoff: 03/31/2017


---

# <a name="configure-a-parallel-activity-in-a-workflow"></a>Paralel bir etkinlik içinde bir iş akışı yapılandırma

Paralel faaliyet yapılandırmak için iş akışı düzenleyicisinde aşağıdaki yordamları tamamlayın.

Paralel faaliyet aynı anda çalışan iş akışı dallarından oluşur.

## <a name="name-a-parallel-activity"></a>Paralel faaliyete ad verme
Paralel faaliyete bir ad vermek için aşağıdaki adımları uygulayın.
1.  Paralel etkinlik sağ tıklatın ve ardından **Özellikler** açmak için **Özellikler** formu.
2.  Sol bölmede **Temel Ayarlar**'a tıklayın.
3.  Paralel faaliyet için **Ad** alanına benzersiz bir ad girin.
4.  **Kapat**'a tıklayın.

## <a name="configure-the-branches-of-a-parallel-activity"></a>Paralel faaliyetin dallarını yapılandırma
Bu paralel faaliyete dal eklemek ve paralel faaliyetin dallarını yapılandırmak için bu adımları izleyin.
1.  Paralel faaliyetin dallarını görüntülemek için paralel faaliyete çift tıklayın.
2.  Dal eklemek için **İş akışı öğeleri** alanından **Dal** öğesini tuval üzerinde bir ekleme noktasına sürükleyin. Aşağıdaki şekil bir ekleme noktasını gösterir.![Ekleme noktası](./media/workflow_insertionpoint.gif)
    | **Not **                                                                                                         |
    |------------------------------------------------------------------------------------------------------------------|
    | Paralel faaliyetin tüm dalları aynı anda çalıştığından dalların sırası önemli değildir. |

3.  Her bir dalı yapılandırmak için bkz. [Paralel dal yapılandırma](http://axhelp.dynamics.com/en/wiki/configure-a-parallel-branch/).




