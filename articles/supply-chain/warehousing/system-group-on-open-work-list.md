---
title: Açık bir iş listesinde sistem gruplama
description: Bu konu, mobil cihazda açık iş listesine nasıl filtre uygulanacağını açıklar.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 73e1da37c354eecf1ef5d44e68d814664fe2be99
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "331978"
---
# <a name="system-grouping-on-an-open-work-list"></a>Açık bir iş listesinde sistem gruplama

[!include [banner](../includes/banner.md)]

Sistem gruplandırma alanını kullanarak, mobil cihaz menü öğesini düzenlemek zorunda kalmadan bir açık iş listesini filtreleyebilirsiniz.
Bu geçerli olduğunda, sistem gruplandırma, tek bir iş başlığı alanındaki bir iş listesini filtrelemek üzere çalışır. Sistem gruplandırmayı satır düzeyindeki alanlarda filtreleme yapmak için kullanamazsınız.

## <a name="set-up-system-grouping-on-an-open-work-list"></a>Açık bir iş listesinde sistem gruplandırmayı ayarlama
Açık bir iş listesinde sistem gruplandırmayı ayarlamak için aşağıdaki adımları uygulayın.

-   Bir mobil cihaz menü öğesinden **Mod: Dolaylı** ve **Faaliyet Kodu: Açık iş listesini görüntüle**'yi seçin. Aşağıdaki seçenekler kullanılabilir olur. Bu seçenekler bir açık iş listesinde sistem gruplandırması için gereklidir. 

|        Seçenek         |                                                                                                                                                                                                                                                                         Açıklama                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sistem gruplandırmaya izin ver |                                                                                                                                                                                                                                                 Seçili iş listesi menü öğesi için sistem gruplandırmayı etkinleştirir.                                                                                                                                                                                                                                                  |
| Sistem gruplandırma alanı | Yalnızca <strong>Sistem işine izin ver</strong> <strong>Evet</strong> olarak ayarlandığında kullanılabilir. Çalışanlar için çekme işinin nasıl gruplanacağını belirleyen bu alanı seçin. Örneğin, <strong>ShipmentId</strong> alanını seçerseniz çalışan çekme işini gruplandırmak için sevkıyat kodunu tarayacaktır. Böylece sevkıyat için tüm iş çalışana atanır. Bu alan, sistem tarafından gruplanan mevcut işi kullanmak için bir menü öğesi oluşturmanızı gerektirir. Çalışanı neyi taraması gerektiği hakkında bilgilendirmek için <strong>Sistem gruplandırma etiketi</strong> alanını kullanın. |
| Sistem gruplandırma etiketi |                       Yalnızca <strong>Sistem işine izin ver</strong> <strong>Evet</strong> olarak ayarlandığında kullanılabilir. Çalışan için çekme işi gruplandırma sırasında neyin taranacağına ilişkin bilgileri girin. Örneğin çekme işini sevkiyata göre gruplandırmak için <strong>ShipmentId</strong> alanını kullanıyorsanız alana Sevkiyat kodu girebilirsiniz. Bu alan, sistem tarafından gruplanan mevcut işi kullanmak için bir menü öğesi oluşturmanızı gerektirir. <strong>Sistem gruplandırma</strong> alanında alanı nasıl gruplandıracağınızı da seçmelisiniz.                       |

