---
title: Kiralama onayı iş akışlarını ayarlama
description: Bu konu, yeni bir kiralama oluşturulduğunda çalışacak bir onay iş akışının nasıl ayarlanacağını açıklar.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0e7280bbf60901266c81a0c89395c5183f991425
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881674"
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
