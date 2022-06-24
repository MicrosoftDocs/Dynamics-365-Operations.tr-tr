---
title: İş emirleri ve sabit kıymetler
description: Bu makalede Kıymet Yönetimi'nde iş emirleri ve sabit kıymetler açıklanmaktadır.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9a6b9cf8327f65371f8362a5729bb32746d900cd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886000"
---
# <a name="work-orders-and-fixed-assets"></a>İş emirleri ve sabit kıymetler

[!include [banner](../../includes/banner.md)]


Varlık Yönetiminde, varlıklar sabit kıymetlerle ilişkilendirilebilir ve bu varlıklar için iş emirleri oluşturabilirsiniz. Bu işlevi kullanırsanız, Microsoft Dynamics 365 for Finance and Operations'da **Proje yönetimi ve muhasebe** ve **Sabit kıymetler** modüllerindeki sabit kıymetlerin, ilgili yatırım projelerinin ve yatırım projelerine kaydedilen maliyetlerin eksiksiz bir genel bakışını alabilirsiniz.

>[!NOTE]
>**Sabit kıymet numarası** alanı, yalnızca iş emri işi projesinde proje türü olarak **Yatırım** türü ayarlanırsa iş emri iş projesinde doldurulur.

Aşağıdaki şekilde, **Proje yönetimi ve muhasebe** modülündeki bir yatırım projesi ile bir iş emri ili projesi arasındaki ilişki gösterilmektedir.

![Şekil 1.](media/24-work-orders.png)

Aşağıdaki prosedürde varlıklar, iş emirleri, iş emri iş projeleri ve sabit kıymetler arasındaki ilişki açıklanmaktadır.

1. Bir sabit kıymetle ilişkilendirdiğiniz bir varlık oluşturursunuz.

![Şekil 2.](media/25-work-orders.png)

2. **İş emri türleri** sayfasında iş emri türlerini (**Varlık yönetimi** > **Kurulum** > **İş emirleri** > **İş emri türleri**) ayarladığınızda yatırımları işlemek için bir iş emri türü oluşturursunuz. Ayrıca bkz. [İş emri türleri](../setup-for-work-orders/work-order-types.md).

![Şekil 3.](media/26-work-orders.png)

3. **İŞ emri proje kurulumu** sayfasının **Proje grubu** sekmesinde iş emri proje grupları (**Varlık yönetimi** > **Kurulum** > **İş emirleri** > **Proje kurulumu**) ayarladığınızda **Proje yönetimi ve muhasebe** modülündeki **Proje grupları** sayfasında (**Proje yönetimi ve muhasebe** > **Kurulum** > **Deftere nakil** > **Proje grupları**) yatırımlar için kullanılan iş emri türü ile yatırımlar için oluşturulan proje grubu arasında bir ilişki oluşturursunuz.

![Şekil 4.](media/27-work-orders.png)

4. Sabit kıymetle ilgili bir iş emri oluşturduğunuzda yatırımları işlemek için kullanılan iş emri türünü (örneğin **Yatırım**) seçin.

5. İş emri oluşturulduğunda ilgili iş emri türü **Tüm iş emirleri** sayfasında gösterilir.

![Şekil 5.](media/28-work-orders.png)

6. İş emri oluşturulduğunda, iş emriyle ilişkili proje, **proje yönetimi ve muhasebe** modülündeki **Tüm projeler** sayfasında oluşturulur (**Proje yönetimi ve muhasebe** > **Projeler** > **Tüm projeler**). Projeyle ilgili bilgileri görüntülemek için, **Varlık yönetimi** modülündeki **Tüm iş emirleri** sayfasının ayrıntılar görünümünde bulunan **Satır ayrıntıları** hızlı sekmesinin **Genel** sekmesindeki **Proje kodu** alanında yer alan bağlantıyı seçin (**Varlık yönetimi** > **Ortak** > **İŞ emirleri** > **Tüm iş emirleri**).

![Şekil 6.](media/29-work-orders.png)

7. Bir sabit kıymetle ilişkili projelerin genel görünümünü görmek için **Sabit kıymetler** > **Sabit kıymetler** > **Sabit kıymetler**'i seçin ve **Sabit kıymet numarası** alanında, ayrıntılar görünümünü açmak için sabit kıymetin bağlantısını seçin. Sayfanın sağ tarafındaki **İlgili bilgi** bölmesini genişletin ve **İlişkili projeler** hızlı sekmesini seçin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]