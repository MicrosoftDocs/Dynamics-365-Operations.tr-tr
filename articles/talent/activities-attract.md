---
title: İşe alım süreçlerine faaliyet ekleme
description: Bu konu, Microsoft Dynamics 365 Talent - Attract işe alma işlemine ekleyebileceğiniz faaliyetlerin çeşitli türleri hakkında bilgi sağlar.
author: hasrivas
manager: AnnBe
ms.date: 05/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: ce8c0bd74a41b9857538b37d0875583d06e8c11d
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124785"
---
# <a name="add-activities-to-a-hiring-process"></a>İşe alım süreçlerine faaliyet ekleme

[!include [banner](includes/banner.md)]

Faaliyetler Microsoft Dynamics 365 Talent: Attract'te işe alma sürecinin bir parçası olarak eklenebilir. Faaliyetler işlem şablonuna eklenebilir veya doğrudan işteki işe alma işlemine eklenebilir. Bir iş tanımlanınca, bir işlem şablonu seçilir ve şablona dahil edilen faaliyetler işe uygulanır. Bir şablon seçili değilse, varsayılan şablon kullanılır. Şablon uygulandıktan sonra işe alma işlemi iş üzerinde değiştirilebilir.

> [!NOTE] 
> İşlem şablonları, Kapsamlı işe alma eklentisinde kullanılabilir. Daha fazla bilgi için bkz. [Hangi Microsoft Dynamics 365 Talent - Attract sürümü](./attract-comprehensive-hiring.md).

## <a name="prospect-activity"></a>Aday müşteri faaliyeti

Aday müşteri faaliyeti, aday müşterilerin bir işe eklenebilir olup olmadığını kontrol eder. Varsayılan olarak, müşteri adayları bir işe eklenebilir. Aday müşteri faaliyetini devre dışı bırakmak için **Müşteri adaylarını etkinleştir** seçeneğini **Kapalı** olarak ayarlayın. Aday müşteri faaliyeti açık olduğunda, işe alma müdürleri müşteri adaylarını ekleyebilir ve görüntüleyebilir, **Aday müşteri** sekmesi iş üzerinde gösterilir.

> [!NOTE]
> Adayların bir işe LinkedIn'den eklenmesine izin vermek için **Aday etkinleştir** seçeneğini **Açık** ayarlamalısınız.

## <a name="application-activity"></a>Başvuru faaliyeti

İşe alma işlem şablonunda Başvuru faaliyeti gereklidir. Başvurularını gönderen veya Başvuru aşamasına eklenen adaylara e-posta göndermek için **Adaya posta gönder** seçeneğini **Açık** olarak ayarlayın.

## <a name="interview-schedule-and-feedback-activity"></a>Planlama ve geribildirim etkinliği

Bu faaliyetin üç bileşeni vardır: Aday erişilebilirlik talebi, Zamanlama ve Geri Bildirim. Adayın uygunluk talebini, zamanlamasını ve geribildirimini, işe alma sürecinin bir parçası olarak tek tek kullanmak yerine işlemin parçası olarak dahil etmek istiyorsanız, iş şablonunda mülakat etkinliğini kullanın. Daha fazla bilgi için bkz. [Mülakat zamanlama ve geribildirim](interview-scheduling-feedback.md).

## <a name="power-apps-activity"></a>Power Apps etkinliği

Power Apps faaliyeti,  Microsoft Power Apps uygulamasını işe alma sürecinize katıştırmanızı sağlar. Uygulama tüm başvuranlar, yalnızca dahili başvuranlar, yalnızca harici başvuranlar veya hiçbir başvuran için gerekli şeklinde ayarlanabilir. Uygulama gerekli olarak işaretlenirse, aşama ileriye taşınmadan önce tamamlanmış olması gerekir. Tamamlandı kabul edilmesi için **JobApplicationStatus** alanının **Tamamlandı** olarak ayarlanması gerekir. Bu alan JobApplicationActivity varlığında bulunmaktadır, böylece Power Apps uygulamasının bu alanı, aşama geçilmeden önce güncelleştirmesi gerekir. Uygulamayı gerekli olarak işaretli değilse, faaliyet isteğe bağlı bir adımdır ve uygulama tamamlanmasa bile aşama ilerleyebilir.

Power Apps faaliyetini işe alma sürecine kaydetmek için bir Power Apps kimliği girmeniz gerekir. Power Apps kimliğini bulmak için [Power Apps](https://web.powerapps.com) adresine gidin, **Uygulamalar**'ı, ardından **Ayrıntılar**'ı seçin.

Varsayılan olarak, Power Apps etkinliği İşe Alma Yöneticisi, İşe Alma Görevlisi ve bunların temsilcilerinin erişimine açıktır. **Bu faaliyet için katılımcı eklenmesine izin ver** seçeneğini belirlerseniz Power Apps faaliyetini kullanan bir uygulama için ek katılımcılar işe alma ekibinden eklenebilir. Örneğin, bir kuruluş teknik görevler için bir görüşme sorusu kitaplığı olan Power Apps uygulaması oluşturdu. Kuruluş şimdi yeni bir yazılım geliştirici işe alıyor ve yazılım geliştirici rolü için işe alma işlemine Power Apps faaliyetini ekledi. **Bu faaliyet için katılımcı eklenmesine izin ver** seçeneği işaretliyse, yazılım geliştirici rolüne başvuranı görüntüleyen bir işveren veya işe alma yöneticisi Power Apps faaliyetine görüşmeciler ekleyebilir. Bu kişiler, görüşme soruları olan uygulamayı daha sonra görebilir.

> [!NOTE]
> Power Apps faaliyeti, yalnızca Kapsamlı işe alım eklentisinde kullanılabilir. Daha fazla bilgi için bkz. [Hangi Microsoft Dynamics 365 Talent - Attract sürümü](./attract-comprehensive-hiring.md).

## <a name="youtube-activity"></a>YouTube etkinliği

YouTube faaliyeti, işe alma işleminin parça olarak YouTube videosu paylaşmanıza olanak sağlar. İşe alma işlemine YouTube faaliyetini kaydetmek için YouTube videosu URL'sini belirtmeniz gerekir. İçeriği **İşe Alım Ekibi**, **Yalnızca Dahili Adaylar**, **Yalnızca Harici adaylar** veya **Tüm Adaylar** olmak üzere görüntülemeyi seçebilirsiniz. Power Apps faaliyeti söz konusu olduğunda, işe alım ekibi katılımcıların faaliyete eklenmesini sağlayabilirsiniz. İçeriği adaylara göstermeyi seçerseniz, video yalnızca aday deneyiminin parçası olarak gösterilir, işe alım sürecinin parçası olarak değil.

> [!NOTE]
> YouTube faaliyeti, yalnızca Kapsamlı işe alım eklentisinde kullanılabilir. Daha fazla bilgi için bkz. [Hangi Microsoft Dynamics 365 Talent - Attract sürümü](./attract-comprehensive-hiring.md).

## <a name="web-content-activity"></a>Web içeriği faaliyeti

Web içeriği faaliyeti, işe alma işlemine çevrimiçi içerik gömmenize olanak tanır. İşe alma işlemine Web içeriği faaliyetini kaydetmek için içeriğin URL'sini belirtmeniz gerekir. İçeriği **İşe Alım Ekibi**, **Yalnızca Dahili Adaylar**, **Yalnızca Harici adaylar** veya **Tüm Adaylar** olmak üzere görüntülemeyi seçebilirsiniz. Power Apps ve YouTube etkinlikleri söz konusu olduğunda, işe alım ekibi katılımcıların faaliyete eklenmesini sağlayabilirsiniz. İçeriği adaylara göstermeyi seçerseniz, Web içeriği yalnızca aday deneyiminin parçası olarak gösterilir, işe alım sürecinin parçası olarak değil. Gösterilen içerik boyutunu seçebilirsiniz.

> [!NOTE]
> Web içeriği faaliyeti, yalnızca Kapsamlı işe alım eklentisinde kullanılabilir. Daha fazla bilgi için bkz. [Hangi Microsoft Dynamics 365 Talent - Attract sürümü](./attract-comprehensive-hiring.md).

## <a name="microsoft-forms-activity"></a>Microsoft Forms faaliyeti

Microsoft Forms etkinliği, Microsoft Forms formunu işe alma işlemine gömmenizi sağlar. Microsoft Forms testler, anketler ve oylamalar oluşturmanıza olanak tanır. İşe alma işlemine Microsoft Forms faaliyetini kaydetmek için formun URL'sini belirtmeniz gerekir. İçeriği **İşe Alım Ekibi**, **Yalnızca Dahili Adaylar**, **Yalnızca Harici adaylar** veya **Tüm Adaylar** olmak üzere görüntülemeyi seçebilirsiniz. Power Apps, YouTube  ve Web içeriği etkinlikleri söz konusu olduğunda, işe alım ekibi katılımcılarının faaliyete eklenmesini sağlayabilirsiniz. İçeriği adaylara göstermeyi seçerseniz, form yalnızca aday deneyiminin parçası olarak gösterilir, işe alım sürecinin parçası olarak değil.

Microsoft Forms'da yazarlar, kurum dışındaki kullanıcıların anket veya testine yanıt verebilmesi için ayarlarını değiştirebilir. Bu durumda, kullanıcılar yanıtlarını anonim olarak gönderir. Anket veya testinizi kimin yaptığını görmek isterseniz yanıtlayanların adlarını anket veya testin bir parçası olarak girmesini isteyebilirsiniz.

> [!NOTE]
> Microsoft Forms faaliyeti, yalnızca Kapsamlı işe alım eklentisinde kullanılabilir. Daha fazla bilgi için bkz. [Hangi Microsoft Dynamics 365 Talent - Attract sürümü](./attract-comprehensive-hiring.md).

## <a name="offer-activity"></a>Teklif etkinliği

İşe alım işlemi şablonu Teklif etkinliğini gerektirir. Tümleştirilmiş teklif yönetimi uygulamasını kullanmak için **Teklif Hazırla içinde Teklif Yönetimi Uygulamasını Başlat**'ı **Açık** olarak ayarlayın. Bu ayar kapalıysa, aday Teklif uygulamasında görüntülenmez, bu nedenle adayın teklif etkinliğine güncelleştirmeleri el ile takip etmeniz gerekir. İşe alım yöneticilerinin aday için teklifi Teklif uygulamasında hazırlayıp hazırlamayacaklarını tanımlamak için **İşe Alım yöneticileri teklif hazırlayabilir**'i **Açık** olarak ayarlayın. İş ile ilişkilendirilmiş birden fazla pozisyon varsa, aynı pozisyon numarasına karşılık birden fazla teklif sunup sunamayacağınıza karar verebilirsiniz. İş başına yalnızca bir teklif sunmak istiyorsanız, **Pozisyonların iş içinde yeniden kullanılmasına izin ver**'i **Kapalı** olarak ayarlayın.

> [!NOTE]
> Tümleştirilmiş Teklif Yönetimi Uygulaması, yalnızca Kapsamlı işe alım eklentisinde kullanılabilir. Daha fazla bilgi için bkz. [Hangi Microsoft Dynamics 365 Talent - Attract sürümü](./attract-comprehensive-hiring.md).


