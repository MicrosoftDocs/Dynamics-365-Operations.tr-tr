---
title: İş akışında paralel etkinlikleri yapılandırma
description: Paralel faaliyet yapılandırmak için iş akışı düzenleyicisinde aşağıdaki yordamları tamamlayın.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2dfbe78f31082ad0b1272f02e3ae9d7adbd993b1
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797738"
---
# <a name="configure-parallel-activities-in-a-workflow"></a>İş akışında paralel etkinlikleri yapılandırma

[!include [banner](../includes/banner.md)]

Paralel faaliyet yapılandırmak için iş akışı düzenleyicisinde aşağıdaki yordamları tamamlayın.

Paralel faaliyet aynı anda çalışan iş akışı dallarından oluşur.

## <a name="name-a-parallel-activity"></a>Paralel faaliyete ad verme

Paralel faaliyete bir ad vermek için aşağıdaki adımları uygulayın.

1. Paralel faaliyete sağ tıklayın ve ardından **Özellikler** formunu açmak için **Özellikler**'e tıklayın.
2. Sol bölmede **Temel Ayarlar**'a tıklayın.
3. Paralel faaliyet için **Ad** alanına benzersiz bir ad girin.
4. **Kapat**'a tıklayın.

## <a name="configure-the-branches-of-a-parallel-activity"></a>Paralel faaliyetin dallarını yapılandırma

Bu paralel faaliyete dal eklemek ve paralel faaliyetin dallarını yapılandırmak için bu adımları izleyin.

1. Paralel faaliyetin dallarını görüntülemek için paralel faaliyete çift tıklayın.
2. Dal eklemek için **İş akışı öğeleri** alanından **Dal** öğesini tuval üzerinde bir ekleme noktasına sürükleyin. Aşağıdaki şekil bir ekleme noktasını gösterir.

    ![Ekleme noktası](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > Paralel faaliyetin tüm dalları aynı anda çalıştığından dalların sırası önemli değildir.

3. Her bir dalı yapılandırmak için bkz. [İş akışında paralel dalları yapılandırma](configure-parallel-branch-workflow.md).
