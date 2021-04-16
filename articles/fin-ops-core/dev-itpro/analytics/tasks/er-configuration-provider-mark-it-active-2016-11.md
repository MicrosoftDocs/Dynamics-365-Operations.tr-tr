---
title: Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme
description: Bu konuda, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolüne atanan bir kullanıcının bir yapılandırma sağlayıcısını nasıl oluşturabileceği açıklanmaktadır.
author: NickSelin
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27e1275199d098fffb56db61ed6bfd2fc3cdb790
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755142"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme

[!include [banner](../../includes/banner.md)]

Bu konu Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolüne atanan bir kullanıcının, Elektronik Raporlama (ER) için bir yapılandırma tedarikçisini nasıl oluşturabileceğini açıklar. Her bir ER yapılandırması, yapılandırmanın yazarı olarak tedarikçiye başvuracaktır. Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma tedarikçisi oluşturacaksınız. Bu adımlar, ER yapılandırma tedarikçileri tüm şirketler arasında paylaşımlı olduğundan herhangi bir şirkette gerçekleştirilebilir.

## <a name="create-a-provider"></a>Sağlayıcı oluşturun
1. Sol üst köşedeki **gezinti bölmesi**'ne gidin ve **Kuruluş yönetimi**'ni seçin.
2. Sırasıyla **Çalışma alanları > Elektronik raporlama**'ya gidin.
3. **İlgili bağlantılar > Yapılandırma sağlayıcılar**'a gidin.
4. **Yeni**'yi seçin.
    - Sağlayıcı kaydı benzersiz bir ada ve URL'ye sahiptir. Bu sayfanın içeriğini gözden geçirin ve Litware, Inc. (https://www.litware.com) için bir kayıt zaten varsa bu yordamı atlayın.  
5. İsim alanına `Litware, Inc.`. yazın.
6. İnternet adresi alanına "`https://www.litware.com`" yazın.
7. **Kaydet**'i seçin.
8. Sayfayı kapatın.

## <a name="select-as-an-active-provider"></a>Etkin bir sağlayıcı olarak seçin
1. Litware, Inc. sağlayıcısını seçin.
2. **Etkin olarak ayarla**'ya tıklayın.

![Elektronik raporlama çalışma alanı sayfası](../media/GER-Task-ActiveProvider-1.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]