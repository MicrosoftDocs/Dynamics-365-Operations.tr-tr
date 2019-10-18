---
title: İş emirleri ve sabit kıymetler
description: Bu konuda Kıymet Yönetimi'nde iş emirleri ve sabit kıymetler açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 95fe394d22f9fe81511c230a2cf7b8ddf00d896f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250842"
---
# <a name="work-orders-and-fixed-assets"></a>İş emirleri ve sabit kıymetler


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Varlık Yönetiminde, varlıklar sabit kıymetlerle ilişkilendirilebilir ve bu varlıklar için iş emirleri oluşturabilirsiniz. Bu işlevi kullanırsanız, **Proje yönetimi ve muhasebe** modülü ve **Sabit kıymetler** modülündeki sabit kıymetlerin, ilgili yatırım projelerinin ve yatırım projelerine kaydedilen maliyetlerin eksiksiz bir genel bakışını görebilirsiniz.

>[!NOTE]
>**Sabit kıymet numarası** alanı, yalnızca iş emri iş projesinde proje türü olarak "Yatırım" türü seçilirse iş emri iş projesinde doldurulur.

![Şekil 1](media/24-work-orders.png)

Aşağıdaki prosedürde varlıklar, iş emirleri, iş emri iş projeleri ve sabit kıymetler arasındaki ilişki açıklanmaktadır.

1. Aşağıdaki şekilde gösterildiği gibi bir sabit kıymetle ilişkilendirmek üzere bir varlık oluşturabilirsiniz.

![Şekil 2](media/25-work-orders.png)

2. İş emri türlerini (**Varlık yönetimi** > **Kurulum** > **İş emirleri** > **İş emri türleri**) ayarladığınızda yatırımları işlemek için bir iş emri türü oluşturursunuz. Ayrıca bkz. [İş emri türleri](../setup-for-work-orders/work-order-types.md).

![Şekil 3](media/26-work-orders.png)

3. İş emri proje grupları (**Varlık yönetimi** > **Kurulum** > **İş emirleri** > **Proje kurulumu** > **Proje grubu** bağlantısı) ayarladığınızda **Proje yönetimi ve muhasebe** modülünde (**Proje yönetimi ve muhasebe** > **Kurulum** > **Deftere nakil** > **Proje grupları**) yatırımlar için kullanılan iş emri türü ile yatırımlar için oluşturulan proje grubu arasında bir ilişki oluşturursunuz.

![Şekil 4](media/27-work-orders.png)

4. Sabit kıymet nesnesiyle ilgili bir iş emri oluşturduğunuzda yatırımları işlemek için kullanılan iş emri türünü (örneğin "yatırım") seçin.

5. İş emri oluşturulduğunda ilgili iş emri türü **Tüm iş emirleri**'nde gösterilir.

![Şekil 5](media/28-work-orders.png)

6. İş emri oluşturulduğunda iş emriyle ilgili proje, **proje yönetimi ve muhasebe** > **Tüm projeler**'de oluşturulur. Projeyle ilgili bilgileri iş emrindeki **Proje kodu** bağlantısına tıklayarak görebilirsiniz (**Varlık yönetimi**'nde, iş emrini Ayrıntılar görünümünde açın > **Satır ayrıntıları** hızlı sekmesi > **Genel** sekmesi > **Proje kodu** alanı).

![Şekil 6](media/29-work-orders.png)

7. **Sabit kıymetler**'de, bir sabit kıymetle ilişkilendirilmiş projelerin genel bakışını görebilirsiniz (**Sabit kıymetler** > **Sabit kıymetler** > **Sabit kıymetler** > **Sabit kıymet sayısı** alanındaki sabit kıymete tıklayın > **İlgili bilgiler** bölmesi > **İlişkili projeler** bölümündeki içerikleri görüntüleyin).

