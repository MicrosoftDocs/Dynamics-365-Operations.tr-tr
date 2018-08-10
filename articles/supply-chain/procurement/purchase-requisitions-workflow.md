---
title: "Satınalma talebi iş akışı"
description: "İş akışı süreci, satın alma talebini, ilk durum olan Taslak durumundan son durum olan Onaylandı durumuna, gözden geçirme sürecine geçirir. Bir satınalma talebi gözden geçirme amacıyla gönderildiğinde iş akışı süreci başlatılır. Bir Satın alma talebi onaylandıktan sonra, satın alma talebi satırları için bir satın alma emri oluşturulabilir ve siparişin gerçekleştirilmesi için satıcıya sunulabilir."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchReqAuthorization, WorkflowParticipantExpenToken
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2234
ms.assetid: dad3ba5a-2892-45d2-874a-300896f59b34
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a5dcc294b3dde7dc7e0f789d9e7678b75bc699b0
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="purchase-requisition-workflow"></a>Satınalma talebi iş akışı

[!include [banner](../includes/banner.md)]

İş akışı süreci, satın alma talebini, ilk durum olan Taslak durumundan son durum olan Onaylandı durumuna, gözden geçirme sürecine geçirir. Bir satınalma talebi gözden geçirme amacıyla gönderildiğinde iş akışı süreci başlatılır. Bir Satın alma talebi onaylandıktan sonra, satın alma talebi satırları için bir satın alma emri oluşturulabilir ve siparişin gerçekleştirilmesi için satıcıya sunulabilir.

Bir satınalma talebinin gözden geçirilmek üzere gönderilebilmesi için bir iş akışı yapılandırmanız gerekir. İş akışı işlemine herhangi bir sırada bir veya daha fazla gözden geçirme adımı eklenebilir. İş akışı işlemi, gözden geçirme görevi atlanacak ve satınalma talebi otomatik olarak onaylanacak şekilde de yapılandırılabilir. İş akışını satınalma talebine tek bir belge olarak yönlendirilecek şekilde yapılandırabilir veya tek tek satınalma talebi satırlarını uygun gözden geçirenlere yönlendirebilirsiniz. Satınalma talebinin bazı gözden geçirenlere tek bir belge olarak yönlendirildiği ve seçilen satınalma talebi satırlarının diğer gözden geçirenlere yönlendirildiği bir senaryo da oluşturabilirsiniz.  

Satınalma talebi satırları tek tek gözden geçirilmişse, iş akışı işleminde sonraki adıma geçilebilmesi için ve satınalma talebi gözden geçirme işlemi bir bütün olarak tamamlanmadan önce gözden geçirme işleminin tamamlanması gerekir. Gözden geçirme işlemi satınalma talepleri ve taleplerin tüm satırları için tamamlandığında, satınalma talebinin genel durumu **Onaylandı** olarak güncellenir.  

İş akışınızı, kuruluşunuzdaki satınalma taleplerine yönelik iş sürecini yansıtacak şekilde yapılandırabilirsiniz. Satınalma talebi iş akışı işleminizi yapılandırırken aşağıdaki soruları göz önünde bulundurun:

-   Hangi harcamaların gözden geçirilmesi gerekir?
-   Hangi harcamalar otomatik olarak onaylanabilir?
-   Harcama isteklerini kimin gözden geçirmesi ve onaylaması gerekir? Bu kullanıcıların atandıkları rol nedir?
-   Bir gözden geçiren uygun değilse, hangi işlem uygulanmalıdır?

Aşağıdaki örnekler, bir iş akışını satınalma talepleri için yapılandırabileceğiniz iki yol gösterir.

## <a name="example-1-route-a-purchase-requisition-as-a-single-document-for-review"></a>Örnek 1: Bir satınalma talebini gözden geçirmek amacıya tek bir belge olarak yönlendirme
Aşağıdaki resim bir satınalma talebinin gözden geçirme amacıyla tek bir belge olarak iş akışına nasıl dahil edileceğini gösterir. Satınalma talebindeki satırlar tek tek yönlendirilmez. Bu örnek için iş akışı sürecine aşağıdaki roller dahil edilir:

-   **Talep sahibi** – Ürün veya hizmet talep eden kullanıcı. Satın alma talebini talep sahibi hazırlayabileceği gibi, satınalma talebini talep sahibinin yerine başka bir çalışan da hazırlayabilir. Bu çalışan hazırlayandır. Hazırlayan, gözden geçirme işlemi süresince satınalma talebinin yönetiminden sorumludur. Yalnızca satınalma talebini hazırlayan kişi onu değiştirebilir.

**Not:** Çalışan başkasının adına bir satınalma talebi oluşturmak için uygun izinlere sahip olmalıdır. Bu izinleri ayarlamak için **Satınalma talebi izni** sayfasını kullanın.

-   **Satınalma aracısı** – Bir tedarik işlemi gerçekleştiren kullanıcı belgeyi gözden geçirebilir ve onaylayabilir.
-   **Talep sahibinin yöneticisi** – Yönetimsel bir inceleme gerçekleştiren ve belgeyi onaylayan kullanıcı.

![Satınalma talebi iş akışını gözden geçirme süreci](./media/purchreqworkflowoverview_submission.gif)  
Bu örnekte, satınalma talepleri için iş akışı süreci aşağıdaki adımları içerir:

1.  Hazırlayan, satınalma talebini gözden geçirilmesi için gönderir.
2.  Satınalma aracısı bir bildirim alır. Bildirim, satınalma aracısının satınalma talebindeki bilgileri doğrulamasını gerektirir. Gerekli bilgiler eksikse, satınalma aracısı onu ekleyebilir ya da satınalma talebini eklemesi için hazırlayana geri gönderebilir. Gerekli tüm bilgiler doldurulduğunda, satınalma talebi gözden geçirme amacıyla bir sonraki adıma taşınabilir.
3.  Talep sahibinin yöneticisi satınalma talebini gözden geçirir. Satınalma talebinin miktarı örneğin talep sahibinin satın alma talebi için belirlediği harcama sınırını aşarsa, satınalma talebi talep sahibinin yöneticisine yönlendirilebilir. Talep sahibinin yöneticisi satınalma talebini onaylayabilir veya reddedebilir ya da değişiklik yapması için hazırlayana geri gönderebilir.

## <a name="example-2-route-the-individual-purchase-requisition-lines-for-review"></a>Örnek 2: Gözden geçirme amacıyla bireysel satınalma talebi satırlarını yönlendirme
Aşağıdaki resim tek tek satınalma talebi satırlarını yönlendirme işleminin bir iş akışına nasıl dahil edileceğini gösterir. Genel olarak, her satırın işlemi tek bir belge olarak gözden geçirilen bir satınalma talebi işleminin aynısıdır. Ancak, iş akışının satınalma talebinin tümü için tamamlanabilmesi için her bir satırın iş akışı işleminin tek tek tamamlanması gerekir.  

Bu örnekte, bir çalışan bir pazarlama kampanyası için poster ve tişört talebi girer. Posterlerin maliyeti Pazarlama departmanı ve Satış departmanı arasında bölünür. Poster ve tişörtlerin maliyeti departman yöneticilerinin imza sınırı yetkisini aşarsa, satınalma talebi grup yöneticisi tarafından da gözden geçirilmelidir.  

Bu örnek için iş akışı sürecine aşağıdaki roller dahil edilir:

-   **Talep sahibi** – Ürün veya hizmet talep eden kullanıcı. Satın alma talebini talep sahibi hazırlayabileceği gibi, satınalma talebini talep sahibinin yerine başka bir çalışan da hazırlayabilir. Bu çalışan hazırlayandır. Hazırlayan, gözden geçirme işlemi süresince satınalma talebinin yönetiminden sorumludur. Yalnızca satınalma talebini hazırlayan kişi onu değiştirebilir.

**Not:** Çalışan başkasının adına bir satınalma talebi oluşturmak için uygun izinlere sahip olmalıdır. Bu izinleri ayarlamak için **Satınalma talebi izni** sayfasını kullanın.

-   **Satınalma aracısı** – Bir tedarik işlemi gerçekleştiren kullanıcı belgeyi gözden geçirebilir ve onaylayabilir.
-   **Talep sahibinin yöneticisi** – Yönetimsel bir inceleme gerçekleştiren ve belgeyi onaylayan kullanıcı.
-   **Departman yöneticisi** – Bir harcama incelemesi gerçekleştiren ve belgeyi onaylayan kullanıcı.
-   **Grup yöneticisi** – İmza yetkisi için bir inceleme gerçekleştiren ve belgeyi onaylayan kullanıcı.

![Satınalma talebi satırı iş akışını gözden geçirme süreci](./media/purchreqlineworkflowoverview.gif)  
Bu örnekte, satınalma talebi satırları için iş akışı süreci aşağıdaki adımları içerir:

1.  Hazırlayan, satınalma talebini gözden geçirilmesi için gönderir. Her satır onu iş akışı işlemine dahil edecek şekilde yapılandıran gözden geçiren kişiye yönlendirilir.
2.  Satınalma aracısı bir bildirim alır. Bildirim, satınalma aracısının satınalma talebindeki ve satınalma talebi satırlarındaki bilgileri doğrulamasını gerektirir. Satınalma temsilcisi tarafından satınalma talebi açıldığında tüm satırlar görünür ancak sanal bir gösterge, hangi satırların satınalma temsilcisine gözden geçirme için gönderildiğini belirtir. Gerekli bilgiler eksikse, satınalma aracısı onu ekleyebilir ya da bir satınalma talebi satırı eklemesi için hazırlayana geri gönderebilir. Gerekli tüm bilgiler doldurulduğunda, satınalma talebi satırı gözden geçirme amacıyla bir sonraki adıma taşınabilir. Satınalma talebi satırları birbirinden bağımsız olarak gözden geçirme sürecine dahil edilebilir.
3.  Talep sahibinin bölüm yöneticisi satınalma talebi satırlarını gözden geçirir ve onaylar. Örneğin satın alma talebi satırındaki miktar talep sahibinin satın alma talebi satırları için belirlediği harcama sınırını aşarsa, onay işlemi satınalma talebi sahibinin yöneticisine yönlendirilebilir. Yönetici, satınalma talebi satırlarının birini veya her ikisini onaylayabilir veya reddedebilir.
4.  Pazarlama departmanı yöneticisi hem posterler hem de tişörtler için satınalma talebi satırlarını gözden geçirir. Satış departmanı yöneticisi, Satış departmanına çıkarılan tek maliyet bu olduğundan yalnızca posterlerim satınalma talebi satırını gözden geçirir.
5.  Grup yöneticisinin onayı gerekiyorsa, grup yöneticisi örneğin satınalma talebi satırındaki tutar departman yöneticisinin onay sınırını aştığından, yalnızca tişörtlerin satınalma talebi satırını gözden geçirir ve onaylar. Grup yöneticisinin posterler için satınalma talebi satırını onaylaması gerekmez.

## <a name="configuring-a-workflow-for-purchase-requisitions"></a>Satınalma talepleri için bir iş akışı yapılandırma
Gözden geçirilmek üzere bir satınalma talebini yönlendirmek için satınalma talebi iş akışı işlemlerini yapılandırmanız gerekir. Tanımladığınız iş akışı işlemi ürünleri, talep eden kullanıcı (talep sahibi) ile iş akışında gözden geçiren ve onaylayan kişi arasındaki etkileşimi denetler. Satınalma talebinin yönlendirilmesi iş akışı yapılandırmasında belirtilen koşullara bağlıdır. Örneğin, bu koşullar satınalma talebinin ne zaman yönlendirilmesi gerektiğini, yönlendirilmesi gereken kullanıcı ile rolü ve kullanıcıları gerçekleştirebileceği işlemleri belirler.  

Bu konudaki örnekler, bir satınalma talebinin bir satınalma talebinin tek bir belge olarak veya bağımsız satınalma talebi satırları olarak bir iş akışı aracılığıyla nasıl yönlendirilebileceğini gösterir. Kuruluşunuz için tanımlanmış satınalma taleplerinin iç denetim incelemesini yansıtan satınalma talepleri için bir iş akışı da yapılandırabilirsiniz.  

Katılımcılar veya bir iş akışında görev atanmış olan gözden geçirenler belirli bir kullanıcı grubunun üyeleri, bir güvenlik rolüne sahip kullanıcılar, yönetimle ilgili hiyerarşide gönderen ile ilişkili kullanıcılar veya adlandırılmış kullanıcılar ya da belirli bir harcama sorumlulukları olan kullanıcılar olabilir.

### <a name="purchase-requisition-expenditure-reviewers"></a>Satınalma talebi harcama gözden geçirenleri

Harcama gözden geçiren kişi yapılandırmaları harcamaları gözden geçirilmesi için dinamik bir şekilde bir proje rolüne veya harcamanın borçlandırıldığı bir mali boyuta atanmış kullanıcıyı temel alır. İş akışı süreci, harcamanın kime yönlendirilmesi gerektiğini belirlemek için belirli bir proje rolünü veya mali boyut sahibini kullanır.  

Bir veya daha fazla harcama gizden geçiren yapılandırması tanımlayabilir ve ardından bir iş akışı oluşturduğunuzda bir yapılandırmayı seçebilirsiniz. Kuruluşunuzdaki her bir tüzel kişilik için harcama gözden geçiren değerlerini yapılandırabilirsiniz. Harcama gözden geçiren yapılandırmalarını tanımladıktan sonra iş akışı görevinize bir yapılandırma atarsınız.  

Harcama gözden geçiren yapılandırmalarını tanımlamanız gerekmez. Bunun yerine, iş akışınızı tanımladığınızda gözden geçirenler olarak belirli kullanıcıları veya kullanıcı gruplarını atayabilirsiniz. Ancak, karmaşık bir kuruluşunuz varsa, harcama gözden geçirenler onay işleminin verimliliğini artırabilir. Buna ek olarak, harcama gözden geçirenlerini ayarlarsanız, bir gözden geçiren iş rolleri her değiştiğinde iş akışı gözden geçiren atamalarını güncelleştirmeniz gerekmez.  

**Satınalma talebi harcama gözden geçirenleri** sayfasında harcama gözden geçirenlerini ayarlayabilirsiniz. Bir harcama gözden geçiren yapılandırması oluşturun ve kuruluşunuzdaki her bir tüzel kişilik için değerler girin. Bir projeye atanan talepler için, talepleri gözden geçirme sorumluluğu olan şu rollerden birini belirtebilirsiniz: Proje yöneticisi, proje denetleyicisi veya Proje satış yöneticisi. Harcamalar belirtilen role atanan kullanıcıya yönlendirilir. **Organizasyon dağıtımları** sekmesinde uygun mali boyut seçeneğini belirleyerek mali boyut sahibine harcama da yönlendirebilirsiniz.  

Bir iş akışında ayarladığınız harcama gözden geçirenlerinin birini kullanmak için, ilgili iş akışı öğesinin **Atamalar** özelliklerinde **Katılımcı türü** seçeneğini **Harcama katılımcıları**  olarak ayarlamanız gerekir.

<a name="additional-resources"></a>Ek kaynaklar
--------

[Tüketim için bir talep oluşturma (Görev kılavuzu)](tasks/create-requisition-consumption.md)

[Satınalma talepleri için iş süreci iş akışları tanımlama](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[Tedarik ve kaynak atama iş akışları](procurement-sourcing-workflows.md)

[Satınalma talebine genel bakış](purchase-requisitions-overview.md)




