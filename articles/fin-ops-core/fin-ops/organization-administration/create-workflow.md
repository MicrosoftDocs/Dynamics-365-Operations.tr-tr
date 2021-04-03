---
title: İş akışlarına genel bakış
description: Bu konu bir iş akışının nasıl oluşturulacağını açıklar.
author: ChrisGarty
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: a64329780b96ca1e1675ced103c86c7cf0bc3754
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567402"
---
# <a name="create-workflows-overview"></a>İş akışlarına genel bakış

[!include [banner](../includes/banner.md)]

Bu konu bir iş akışının nasıl oluşturulacağını açıklar.

## <a name="open-the-workflow-editor"></a>İş akışı düzenleyicisini açma

Oluşturabileceğiniz iş akışı türleri, çalışmakta olduğunuz modüle göre belirlenir. Oluşturmak için iş akışı türünü seçmek ve iş akışı düzenleyicisini açmak için aşağıdaki adımları izleyin.

1. Yeni bir iş akışı oluşturmak istediğiniz modülü açın. Örneğin, satınalma talepleri için bir iş akışı oluşturmak için **Tedarik ve kaynak atama**'ya tıklayın.
2. **Kurulum** &gt; **\[Modül adı\] iş akışları'na** tıklayın.
3. Eylem Bölmesi'nde görüntülenen liste sayfasında **Yeni**'ye tıklayın.
4. **İş akışı oluştur** sayfasında oluşturmak için iş akışı türünü seçin ve ardından **İş akışı oluştur**'a tıklayın. İş akışı düzenleyicisi görüntülenir. İş akışını tasarlamak için artık aşağıdaki yordamları kullanabilirsiniz.

## <a name="drag-workflow-elements-onto-the-canvas"></a>İş akışı öğelerini tuval üzerine sürükleme

İş akışı düzenleyicisinin **İş akışı öğeleri** alanı iş akışınıza ekleyebileceğiniz öğeler içerir. Öğeleri iş akışına eklemek için tuval üzerine sürükleyin.

## <a name="connect-the-elements"></a>Öğeleri bağlama

İş akışı öğesini bir başkasına bağlamak için işaretçiyi bağlantı noktaları görünene kadar öğenin üstünde tutun. Bağlantı noktasına tıklayın ve bir başka öğeye sürükleyin. Tüm öğeleri bağladığınızdan emin olun.

## <a name="configure-the-properties-of-the-workflow"></a>İş akışının özelliklerini yapılandırma

İş akışının özelliklerini yapılandırmak için aşağıdaki adımları izleyin.

1. Herhangi bir iş akışı öğesinin seçili olmadığından emin olmak için tuvale tıklayın.
2. İş akışı için **Özellikler** sayfasını açmak için **Özellikler**'e tıklayın.
3. [İş akışı özelliklerini yapılandırma](configure-workflow-properties.md) konusundaki prosedürleri uygulayın.

## <a name="configure-the-elements-of-the-workflow"></a>İş akışının öğelerini yapılandırma

Tuvalin üzerine sürüklediğiniz tüm öğeleri yapılandırın. Tüm iş akışı öğelerini nasıl yapılandıracağınız hakkında daha fazla bilgi için aşağıdaki konulara bakın:

- [İş akışında el ile girilen görevleri yapılandırma](configure-manual-task-workflow.md)
- [İş akışında otomatikleştirilmiş görevleri yapılandırma](configure-automated-task-workflow.md)
- [İş akışında onay işlemlerini yapılandırma](configure-approval-process-workflow.md)
- [İş akışında onay adımlarını yapılandırma](configure-approval-step-workflow.md)
- [İş akışında el ile girilen kararları yapılandırma](configure-manual-decision-workflow.md)
- [İş akışında koşullu kararları yapılandırma](configure-conditional-decision-workflow.md)
- [İş akışında paralel dalları yapılandırma](configure-parallel-activity-workflow.md)
- [Paralel dalı yapılandırma](configure-parallel-branch-workflow.md)
- [Satır maddesi iş akışlarını yapılandırma](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a>Hatalar veya uyarıları çözümleme

İş akışı düzenleyicisinin altındaki **Hatalar ve uyarılar** bölmesi iş akışı için oluşturulan iletileri gösterir. Hatanın veya uyarının nerede oluştuğunu bulmak için hata veya uyarı iletisine çift tıklayın. İş akışını etkin hale getirmeden önce tüm hataları ve uyarıları çözümlemeniz gerekir.

## <a name="save-and-activate-the-workflow"></a>İş akışını kaydetme ve etkinleştirme

İş akışını kaydetmek ve etkinleştirmek için hazır olduğunuzda bu adımları izleyin.

1. İş akışı düzenleyicisini kapatmak için **Kaydet ve kapat**'a tıklayın ve **İş akışını kaydet** sayfasını açın.
2. İş akışında yaptığınız değişiklikler hakkında yorumlar girin ve ardından **Tamam**'a tıklayın.
3. Tüm hatalar ve uyarılar çözümlenirse **İş akışını etkinleştir** sayfası görüntülenir. Aşağıdaki seçeneklerden birini belirleyin:

    - İş akışının bu sürümünü etkinleştirmek için **Yeni sürümü etkinleştir**'e tıklayın. İş akışı etkinken kullanıcılar işlenmesi için iş akışına belgeler gönderebilir.
    - Bu sürümü etkinleştirmek istemiyorsanız **Yeni sürümü etkinleştirme**'ye tıklayın. İş akışını daha sonra etkinleştirebilirsiniz.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]