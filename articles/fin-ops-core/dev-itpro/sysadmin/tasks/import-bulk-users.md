---
title: Azure Active Directory'den kullanıcıları içeri aktarma
description: Bu yordam, sistem yöneticisi tarafından Azure Active Directory'den seçili kullanıcıları el ile içeri aktarma veya çok sayıda kullanıcıyı içeri aktarma için kullanılabilir.
author: peakerbl
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0c2600ad8f441e6b73b143c27afa08ad0a5c2748
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571017"
---
# <a name="import-users-from-azure-active-directory"></a>Azure Active Directory'den kullanıcıları içeri aktarma

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a>Seçili kullanıcıları içeri aktarma

Bu yordam, sistem yöneticisi tarafından Azure Active Directory'den (Azure AD) seçili kullanıcıları içeri aktarmak için kullanılabilir.

1. Kullanıcı içeri aktarılırken geçerli oturum şirketi varsayılan şirketi olur. Gerekirse kullanıcıları içeri aktarmadan önce geçerli şirketi değiştirin.
2. **Sistem yönetimi > Kullanıcılar > Kullanıcı** bölümüne gidin.
3. **Kullanıcıları içe aktar**'a tıklayın.
4. İçeri aktarılması gereken kullanıcıları seçin ve **Kullanıcıları içe aktar**'ı seçin.

İçeri aktarma işlemi tamamlandıktan sonra, kullanıcılara rol atanması gerekir.

## <a name="import-users-in-bulk"></a>Kullanıcıları topluca içe aktarma

Bu yordam, sistem yöneticisi tarafından çok sayıda kullanıcıyı Azure Active Directory'den almak için kullanılabilir.
Toplu içeri aktarma seçeneğini kullanırken kullanıcı seçmek mümkün değildir.

## <a name="run-the-import-as-a-batch-job"></a>İçeri aktarmayı toplu iş olarak çalıştırma
1. Kullanıcı içeri aktarılırken geçerli oturum şirketi varsayılan şirketi olur. Gerekirse kullanıcıları içeri aktarmadan önce geçerli şirketi değiştirin.
2. **Sistem yönetimi > Kullanıcılar > Kullanıcılar** bölümüne gidin.
3. **Toplu içe aktarma**'ya tıklayın.
4. **Arka planda çalıştır** bölümünü genişletin.
4. **Toplu işlem** alanında **Evet** seçeneğini seçin.
6. **Toplu iş grubu** alanında bir değer girin veya bir değer seçin. Bu isteğe bağlı bir adımdır.  
7. **Özel** alanında **Evet**'i seçin. Bu isteğe bağlı bir adımdır.  
8. **Kritik iş** alanında **Evet**'i seçin. Bu isteğe bağlı bir adımdır.  
9. **İzleme kategorisi** alanında bir seçenek belirleyin.
10. **Tamam**'a tıklayın.

İçeri aktarma işlemi tamamlandıktan sonra, kullanıcılara rol atanmalıdır.

## <a name="run-in-a-sandbox-environment"></a>Bir korumalı alan ortamında çalıştırın
1. **Toplu içeri aktarma**'yı seçin.
2. **Tamam**'ı seçin.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]