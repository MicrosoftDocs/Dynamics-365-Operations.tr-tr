---
title: Süreçlerdeki faaliyetler
description: Bu konu, işe alma işleminde kullanılabilecek faaliyetlerin çeşitli türleri hakkında bilgi sağlar.
author: ''
manager: AnnBe
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c32db1f563466f05b9fef1a03578392888c0b7e6
ms.sourcegitcommit: 1e32d78868098fd76124bb41363f15c4ec3ea15a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2019
ms.locfileid: "374769"
---
# <a name="activities-in-the-hiring-processes"></a>İşe alım süreçlerindeki faaliyetler

[!include[banner](../includes/banner.md)]

Faaliyetler beceri için Microsoft Dynamics 365 for Talent: Attract'te işe alma işleminin bir parçası olarak eklenebilir. Faaliyetler işlem şablonuna eklenebilir veya doğrudan işteki işe alma işlemine eklenebilir. Bir iş tanımlanınca, bir işlem şablonu seçilir ve şablona dahil edilen faaliyetler işe uygulanır. Bir şablon seçili değilse, varsayılan şablon kullanılır. Şablon uygulandıktan sonra işe alma işlemi iş üzerinde değiştirilebilir.

> [!NOTE] 
> İşlem şablonları, Kapsamlı işe alma eklentisinde kullanılabilir.

## <a name="prospect-activity"></a>Aday müşteri faaliyeti

Aday müşteri faaliyeti, aday müşterilerin bir işe eklenebilir olup olmadığını kontrol eder. Varsayılan olarak, müşteri adayları bir işe eklenebilir. Aday müşteri faaliyetini devre dışı bırakmak için **Müşteri adaylarını etkinleştir** seçeneğini **Kapalı** olarak ayarlayın. Aday müşteri faaliyeti açık olduğunda, işe alma müdürleri müşteri adaylarını ekleyebilir ve görüntüleyebilir, **Aday müşteri** sekmesi iş üzerinde gösterilir.

## <a name="application-activity"></a>Başvuru faaliyeti

İşe alma işlem şablonunda Başvuru faaliyeti gereklidir. Başvurularını gönderen veya Başvuru aşamasına eklenen adaylara e-posta göndermek için **Adaya posta gönder** seçeneğini **Açık** olarak ayarlayın.

## <a name="interview-schedule-and-feedback-activity"></a>Planlama ve geribildirim etkinliği

Bu faaliyetin üç bileşeni vardır: Aday erişilebilirlik talebi, Zamanlama ve Geri Bildirim. Adayın uygunluk talebini, zamanlamasını ve geribildirimini, işe alma sürecinin bir parçası olarak tek tek kullanmak yerine işlemin parçası olarak dahil etmek istiyorsanız, iş şablonunda mülakat etkinliğini kullanın. Daha fazla bilgi için bkz. [Mülakat zamanlama ve geribildirim](interview-scheduling-feedback.md).

## <a name="powerapps-activity"></a>PowerApps faaliyeti

PowerApps faaliyeti, Microsoft PowerApps uygulamasını işe alma işlemine gömmenizi sağlar. Uygulama tüm başvuranlar, yalnızca dahili başvuranlar, yalnızca harici başvuranlar veya hiçbir başvuran için gerekli şeklinde ayarlanabilir. Uygulama gerekli olarak işaretlenirse, aşama ileriye taşınmadan önce tamamlanmış olması gerekir. Uygulamayı gerekli olarak işaretli değilse, faaliyet isteğe bağlı bir adımdır ve uygulama tamamlanmasa bile aşama ilerleyebilir.

PowerApps faaliyetini işe alma sürecini kaydetmek için bir PowerApps kimliği girmeniz gerekir. PowerApps kimliği bulmak için [PowerApps](https://web.powerapps.com) adresine gidin, **Uygulamalar**'ı, ardından **Ayrıntılar**'ı seçin.

**Bu faaliyet için katılımcı eklenmesine izin ver** seçeneğini belirlerseniz PowerApps kullanan bir uygulama için ek katılımcılar eklenebilir. Örneğin, bir kuruluş teknik görevler için bir görüşme sorusu kitaplığı olan PowerApps uygulaması oluşturdu. Kuruluş şimdi yeni bir yazılım geliştirici işe alıyor ve yazılım geliştirici rolü için işe alma işlemine PowerApps faaliyeti ekledi. **Bu faaliyet için katılımcı eklenmesine izin ve** seçeneği işaretliyse, yazılım geliştirici rolüne başvuranı görüntüleyen bir işveren veya işe alma yöneticisi PowerApps faaliyetine kişiler ekleyebilir. Bu kişiler, görüşme soruları olan uygulamayı daha sonra görebilir.

> [!NOTE]
> PowerApps faaliyeti, yalnızca Kapsamlı işe alım eklentisinde kullanılabilir.

## <a name="youtube-activity"></a>YouTube etkinliği

YouTube faaliyeti, işe alma işleminin parça olarak YouTube videosu paylaşmanıza olanak sağlar. İşe alma işlemine YouTube faaliyetini kaydetmek için YouTube videosu URL'sini belirtmeniz gerekir. PowerApps faaliyeti söz konusu olduğunda, katılımcıların faaliyete eklenmesini sağlayabilirsiniz. **Yalnızca adaya göster** seçeneğini belirlerseniz video yalnızca aday deneyimi parçası olarak gösterilir. Attract'taki işe alma işleminde gösterilmez.

> [!NOTE]
> YouTube faaliyeti, yalnızca Kapsamlı işe alım eklentisinde kullanılabilir.

## <a name="web-content-activity"></a>Web içeriği faaliyeti

Web içeriği faaliyeti, işe alma işlemine çevrimiçi içerik gömmenize olanak tanır. İşe alma işlemine Web içeriği faaliyetini kaydetmek için içeriğin URL'sini belirtmeniz gerekir. PowerApps ve YouTube faaliyeti söz konusu olduğunda, katılımcıların faaliyete eklenmesini sağlayabilirsiniz. **Yalnızca adaya göster** seçeneğini belirlerseniz içerik yalnızca aday deneyimi parçası olarak gösterilir. Attract'taki işe alma işleminde gösterilmez. Gösterilen içerik boyutunu seçebilirsiniz.

> [!NOTE]
> Web içeriği faaliyeti, yalnızca Kapsamlı işe alım eklentisinde kullanılabilir.

## <a name="microsoft-forms-activity"></a>Microsoft Forms faaliyeti

Microsoft Forms faaliyeti, Microsoft Forms formunu işe alma işlemine gömmenizi sağlar. Microsoft Forms testler, anketler ve oylamalar oluşturmanıza olanak tanır. İşe alma işlemine Microsoft Forms faaliyetini kaydetmek için formun URL'sini belirtmeniz gerekir. PowerApps, YouTube ve Web içeriği faaliyeti söz konusu olduğunda, katılımcıların faaliyete eklenmesini sağlayabilirsiniz. **Yalnızca adaya göster** seçeneğini belirlerseniz form yalnızca aday deneyimi parçası olarak gösterilir. Attract'taki işe alma işleminde gösterilmez.

Microsoft Forms'da yazarlar, kurum dışındaki kullanıcıların anket veya testine yanıt verebilmesi için ayarlarını değiştirebilir. Bu durumda, kullanıcılar yanıtlarını anonim olarak gönderir. Anket veya testinizi kimin yaptığını görmek isterseniz yanıtlayanların adlarını anket veya testin bir parçası olarak girmesini isteyebilirsiniz.

> [!NOTE]
> Microsoft Forms faaliyeti, yalnızca Kapsamlı işe alım eklentisinde kullanılabilir.
