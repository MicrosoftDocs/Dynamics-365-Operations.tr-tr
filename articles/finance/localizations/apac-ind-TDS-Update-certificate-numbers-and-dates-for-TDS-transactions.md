---
title: TDS işlemleri için sertifika numaralarını ve tarihleri güncelleme
description: Bu makalede; Kaynakta Kesilen Vergide (TDS) satıcı, müşteri ve genel muhasebe hesapları için kaydedilen düşürülebilir sertifika numaralarının nasıl güncelleştirileceği açıklanmaktadır.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 147a27261a4a282550f0bacede78c9edd38b4fe6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904455"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a>TDS işlemleri için sertifika numaralarını ve tarihleri güncelleme

[!include [banner](../includes/banner.md)]

Bu makalede; Kaynakta Kesilen Vergide (TDS) satıcı, müşteri ve genel muhasebe hesapları için kaydedilen düşürülebilir sertifika numaralarının nasıl güncelleştirileceği açıklanmaktadır. TDS hareketleriyle ilgili sertifikaları **Düşürülebilir sertifikaları** sayfasında görüntüleyebilirsiniz. **Sertifikaları Güncelleştir** sayfasını kullanarak sertifikaları güncelleştirebilirsiniz.

TDS hareketleri için sertifika numaralarını ve tarihlerini güncelleştirmek için aşağıdaki adımları izleyin.

1. **Vergi \> Beyanlar \> Stopaj vergisi \> Sertifikayı güncelleştir**'e gidin.

    [![Sertifikayı güncelleştir sayfası.](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)

2. **Sertifikayı güncelleştir** sayfasında, **Seçim** bölümünde, **Vergi türü** alanında, **TDS**'yi seçin.
3. **Sertifika numarası** alanında, müşterinin veya satıcının TDS sertifika numarasını seçin.

    > [!NOTE]
    > **Sertifika numarası** alanı, yalnızca **Düşürülebilir sertifikaları** sayfasında **Kapalı** onay kutusunun seçili olmadığı TDS sertifika numaralarını listeler.

    **Sertifika tarihi** alanı, sertifika tarihini gösterir. **Hesap türü** alanı, TDS sertifika numarasının hangi hesap türü için alındığını gösterirken **Ad** alanında hesabın adı gösterilir.

5. **Başlangıç tarihi** ve **Bitiş tarihi** alanlarında, TDS hareketlerini görüntülemek için dönemin başlangıç ve bitiş tarihlerini seçin.
6. Seçili dönemde deftere nakledilen TDS hareketlerini görüntülemek için **Verileri göster**'i seçin.

    **Genel bakış** sekmesinde, üst bölmedeki ızgara, seçilen dönemde satıcı veya müşteri için deftere nakledilen her TDS hareketiyle ilgili aşağıdaki bilgileri gösterir:

    - **Fiş** – TDS hareketinin fiş numarasını görüntüler.
    - **Tarih** - TDS hareketinin tarihi.
    - **Tutar** – TDS'nin üzerinde hesaplandığı fatura tutarı.
    - **Vergi tutarı** – Hareket için hesaplanan TDS vergi tutarı.

7. Belirli TDS hareketlerini üst ızgaradan aşağı ızgaraya taşımak için, hareketleri seçin ve **Dahil et**'i seçin. Alternatif olarak, Tüm TDS hareketlerini üst ızgaradan aşağı ızgaraya taşımak için **Tümünü dahil et**'i seçin.

    Belirli TDS hareketlerini veya tüm TDS hareketlerini alt ızgaradan üst ızgaraya taşımak için, **Hariç tut** veya **Tümünü hariç tut** düğmesini kullanın.

8. TDS hareketleri için alt ızgaradaki **Sertifika numarası** ve **Sertifika tarihi** alanlarını güncelleştirmek için **Güncelleştir**'i seçin.
10. **Vergi \> Dolaylı vergiler \> Stopaj vergisi \> Düşürülebilir sertifikası**'na gidin ve **Sertifika hareketleri** sayfasında yeni sertifika numaralarına sahip güncelleştirilmiş hareket satırlarını görüntülemek için **Sorgulama**'yı seçin.

    [![Sertifika hareketleri sayfası.](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)
