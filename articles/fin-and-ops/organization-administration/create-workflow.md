---
title: "İş akışı oluşturma"
description: "Bu konu bir iş akışının nasıl oluşturulacağını açıklar."
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ee3f60575d0eaaf56ce08adb1936728a76488dac
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="create-a-workflow"></a>İş akışı oluşturma

[!include [banner](../includes/banner.md)]

Bu konu bir iş akışının nasıl oluşturulacağını açıklar.

<a name="open-the-workflow-editor"></a>İş akışı düzenleyicisini açma
------------------------

Oluşturabileceğiniz iş akışı türleri, çalışmakta olduğunuz Microsoft Dynamics 365 for Finance and Operations modülüne göre belirlenir. Oluşturmak için iş akışı türünü seçmek ve iş akışı düzenleyicisini açmak için aşağıdaki adımları izleyin.

1.  Yeni bir iş akışı oluşturmak istediğiniz modülü açın. Örneğin, satınalma talepleri için bir iş akışı oluşturmak için **Tedarik ve kaynak atama**'ya tıklayın.
2.  **Kurulum** &gt; **\[Modül adı\] iş akışları'na** tıklayın.
3.  Eylem Bölmesi'nde görüntülenen liste sayfasında **Yeni**'ye tıklayın.
4.  **İş akışı oluştur** sayfasında oluşturmak için iş akışı türünü seçin ve ardından **İş akışı oluştur**'a tıklayın. İş akışı düzenleyicisi görüntülenir. İş akışını tasarlamak için artık aşağıdaki yordamları kullanabilirsiniz.

## <a name="drag-workflow-elements-onto-the-canvas"></a>İş akışı öğelerini tuval üzerine sürükleme
İş akışı düzenleyicisinin **İş akışı öğeleri** alanı iş akışınıza ekleyebileceğiniz öğeler içerir. Öğeleri iş akışına eklemek için tuval üzerine sürükleyin.

## <a name="connect-the-elements"></a>Öğeleri bağlama
İş akışı öğesini bir başkasına bağlamak için işaretçiyi bağlantı noktaları görünene kadar öğenin üstünde tutun. Bağlantı noktasına tıklayın ve bir başka öğeye sürükleyin. Tüm öğeleri bağladığınızdan emin olun.

## <a name="configure-the-properties-of-the-workflow"></a>İş akışının özelliklerini yapılandırma
İş akışının özelliklerini yapılandırmak için aşağıdaki adımları izleyin.

1.  Herhangi bir iş akışı öğesinin seçili olmadığından emin olmak için tuvale tıklayın.
2.  İş akışı için **Özellikler** sayfasını açmak için **Özellikler**'e tıklayın.
3.  [İş akışının özelliklerini yapılandırma](configure-workflow-properties.md) konusundaki yordamları uygulayın.

## <a name="configure-the-elements-of-the-workflow"></a>İş akışının öğelerini yapılandırma
Tuvalin üzerine sürüklediğiniz tüm öğeleri yapılandırın. Tüm iş akışı öğelerini nasıl yapılandıracağınız hakkında daha fazla bilgi için aşağıdaki konulara bakın:

-   [El ile girilen bir görev yapılandırma](configure-manual-task-workflow.md)
-   [Otomatik bir görev yapılandırma](configure-automated-task-workflow.md)
-   [Onay süreci konfigüre etme](configure-approval-process-workflow.md)
-   [Onay adımını yapılandırma](configure-approval-step-workflow.md)
-   [El ile girilen kararı yapılandırma](configure-manual-decision-workflow.md)
-   [Koşullu kararı yapılandırma](configure-conditional-decision-workflow.md)
-   [Paralel faaliyeti yapılandırma](configure-parallel-activity-workflow.md)
-   [Paralel dal yapılandırma](configure-parallel-branch-workflow.md)
-   [Satır maddesi iş akışı yapılandırma](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a>Hatalar veya uyarıları çözümleme
İş akışı düzenleyicisinin altındaki **Hatalar ve uyarılar** bölmesi iş akışı için oluşturulan iletileri gösterir. Hatanın veya uyarının nerede oluştuğunu bulmak için hata veya uyarı iletisine çift tıklayın. İş akışını etkin hale getirmeden önce tüm hataları ve uyarıları çözümlemeniz gerekir.

## <a name="save-and-activate-the-workflow"></a>İş akışını kaydetme ve etkinleştirme
İş akışını kaydetmek ve etkinleştirmek için hazır olduğunuzda bu adımları izleyin.

1.  İş akışı düzenleyicisini kapatmak için **Kaydet ve kapat**'a tıklayın ve **İş akışını kaydet** sayfasını açın.
2.  İş akışında yaptığınız değişiklikler hakkında yorumlar girin ve ardından **Tamam**'a tıklayın.
3.  Tüm hatalar ve uyarılar çözümlenirse **İş akışını etkinleştir** sayfası görüntülenir. Aşağıdaki seçeneklerden birini belirleyin:
    -   İş akışının bu sürümünü etkinleştirmek için **Yeni sürümü etkinleştir**'e tıklayın. İş akışı etkinken kullanıcılar işlenmesi için iş akışına belgeler gönderebilir.
    -   Bu sürümü etkinleştirmek istemiyorsanız **Yeni sürümü etkinleştirme**'ye tıklayın. İş akışını daha sonra etkinleştirebilirsiniz.






