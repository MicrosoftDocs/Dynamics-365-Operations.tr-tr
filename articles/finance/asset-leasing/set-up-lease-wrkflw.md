---
title: Kiralama onayı iş akışlarını ayarlama
description: Bu konu, yeni bir kiralama oluşturulduğunda çalışacak bir onay iş akışının nasıl ayarlanacağını açıklar.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1eaa2f5cc191ec93c30f4f10a662a87e501a341d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249593"
---
# <a name="set-up-lease-approval-workflows"></a>Kiralama onayı iş akışlarını ayarlama

[!include [banner](../includes/banner.md)]

Bu konu, yeni bir kiralama oluşturulduğunda çalışacak bir onay iş akışının nasıl ayarlanacağını açıklar. İş akışının nasıl kullanılacağı hakkında bilgi için bkz. [Kiralama onayı iş akışlarını kullanma](use-create-lease-wrkflw.md). 

1. **Varlık kiralama \> Kurulum \> Kiralama iş akışı**'na gidin.
2. **Kiralama iş akışı** sayfasında **Yeni**'yi seçin.
3. Görüntülenen iletişim kutusunda, **İş akışı türünde** **Kiralama iş akışı** bağlantısını seçin.

    Uygulama açıldı. Çalıştıktan sonra iş akışı uygulamasına yönlendirilmek için Azure Active Directory'de (Azure AD) oturum açın.

4. **Kiralama iş akışı onayı** öğesini iş akışının üzerine sürükleyin.
5. **Başlangıç**'tan **Kiralama iş akışı onayı**'na bir düğüm bağlayın. Ardından **Kiralama iş akışı onayı**'nı **Bitiş**'e bağlayın.
6. **Kiralama iş akışı onayı**'na çift tıklayın.
7. **Özellikler**'i seçin ve **Temel ayarlar** bölümünde iş akışı için bir ad girin.

    Bu sayfada, iş akışı için daha fazla parametre ayarlayabilirsiniz. **Otomatik eylemleri** etkinleştirdiyseniz , sistem otomatik olarak belirli bir eylemi alacaktır. **Bildirimler** sekmesinde etkinleştirildiyse bildirim gönderilebilir. **Gelişmiş ayarlar** sekmesinde nihai onaylacıyı belirtebilir, süre sınırı ayarlayabilir ve tamamlanması gereken belirli eylemler atayabilirsiniz.

8. İş akışı parametrelerini ayarlamayı bitirdiğinizde **Kapat**'ı seçin.
9. **Adım 1**'i seçin ve ardından **Özellikler**'i seçin.
10. **Temel ayarlar** bölümünde adım için bir ad girin, onay için bir konu satırı oluşturun ve onay için yönergeler belirtin.
11. **Atama** sayfasında, atama türünü seçin.
12. Onaya belirli kullanıcılar atamak için **Kullanıcı**'yı seçin, kiralamaları onaylayan kullanıcıları seçin ve ardından **Kapat**'ı seçin.
13. İş akışını oluşturmak için **Kaydet ve kapat**'ı seçin. Ardından, istendiğinde **Tamam**'ı seçin.
14. **İş akışı oluştur** sayfasında **Kapat**'ı seçin.
14. Yeni iş akışını seçin ve ardından **Sürümler**'i seçin. İş akışının etkin olmasını sağlamak için **Etkinleştir**'i seçin.
15. **Kapat**'ı seçin. Yeni etkin sürüm görüntülenir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]