---
title: Genel muhasebe fişlerinde dahili verilere yapılan düzenlemelere izin ver
description: Bu makale, genel muhasebe fişindeki dahili verilerin nasıl düzenleneceği hakkında bilgi sağlar.
author: kweekley
ms.date: 08/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 26fc6518f0b4eae815e047db1dbaadd7c56a2e67
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220674"
---
# <a name="allow-edits-to-internal-data-on-general-ledger-vouchers"></a>Genel muhasebe fişlerinde dahili verilere yapılan düzenlemelere izin ver

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]


Muhasebe girişlerini genel muhasebeye naklettiğinizde **Açıklama** alanı, dahili notları veya belgeleri depolamak için sık kullanılır. Bilgiler yanlışsa, karışıklığa neden olabilir ve dönem sonu kapanışı daha zor olabilir. Bu özellik, genel muhasebedeki deftere nakledilen fişlerle ilgili **Açıklama** alanını düzenleyerek muhasebe yöneticisinin veya muhasebe gözetmeninin hataları gidermelerini sağlar.

Genel muhasebedeki deftere nakledilen fişlerle ilgili değişiklikler, dahili olan verilerle sınırlıdır. Bu özellik, tutarlar, deftere nakil tarihleri, genel muhasebe hesapları ve hareket para birimi gibi verileri düzenlemenize hiçbir zaman izin vermez. Bu verilerde yapılan değişiklikler mali tabloların harici raporlamasını etkiler ve yalnızca yeni genel muhasebe fişleri üzerinden yapılmalıdır.

> [!NOTE]
> Dynamics 365 Finance sürüm 10.0.29 için bu özellik, **Açıklama** alanındaki düzenlemelerle sınırlıdır.

## <a name="edit-internal-data-on-general-ledger-vouchers"></a>Genel muhasebe fişlerindeki dahili verileri düzenleme

Genel muhasebe fişindeki dahili verilerin düzenlenebilmesi için önce, **Özellik yönetimi** çalışma alanında **Genel muhasebe fişlerinde dahili verilere yapılan düzenlemelere izin ver** özelliğini etkinleştirmeniz gerekir.
Özellik etkinleştirildikten sonra, deftere nakledilen fişleri düzenleyebilecek olan kullanıcı Muhasebe Yöneticisi veya Muhasebe Gözetmeni rolüne atanmalıdır. Güvenlik rollerini özelleştirerek diğer rollere de izin ekleyebilirsiniz.

Düzenleme işlemine yalnızca Fiş hareketleri sayfasında izin verilir.

1. **Genel muhasebe** > **Sorgular ve raporlar** > **Fiş hareketleri**'ne gidin.
2. **SysQuery** iletişim kutusunda, fişleri seçmek için arama ölçütünü girin.
3. Düzenlemek istediğiniz fişlerle ilgili satırları seçin ve **Fiş düzenle** > **Dahili fiş verilerini düzenle**'yi seçin.

    [![Fiş hareketleri sayfası.](./media/voucher-transactions-page.png)](./media/voucher-transactions-page.png)
    
**Dahili fiş verilerini düzenle** sayfasında, seçtiğiniz her satır için aşağıdaki veriler gösterilir:
  
  - Genel muhasebe hesabı
  - Hesap adı
  - Fiş
  - Mevcut açıklama
  - Yeni açıklama

    [![Günlük fişi.](./media/edit-internal-voucher-data.png)](./media/edit-internal-voucher-data.png)
    
> [!NOTE]
> Yalnızca **Yeni açıklama** alanı düzenlenebilir. Varsayılan olarak değer, açıklamada önemsiz hataları hızlı şekilde düzeltmek için **Geçerli açıklama** alanı değeriyle eşleştirilir.

4. Her satırdaki **Yeni açıklama** alanını değiştirin veya her satırdan açıklamayı silin.

   Alternatif olarak, birden fazla satır aynı değerle güncelleştiriliyorsa şu adımları izleyin:

      1. Düzenlenecek satırları seçin ve **Seçilen kayıtları toplu güncelleştir**'i seçin.
      2. **Düzenlenecek alan** alanında, düzenlenecek alanı seçin. Şu anda arama yalnızca **Yeni açıklama** alanını içermektedir.
      3. **Yeni değer** alanına yeni bir açıklama girin.
      4. **Güncelleştir**'i seçin Seçilen tüm kayıtlar yeni değerle güncelleştirilir.

      [![Seçilen kayıtları toplu güncelleştir iletişim kutusu.](./media/bulk-update-selected-records.png)](./media/bulk-update-selected-records.png)
    
5. **Düzenleme nedeni** alanına, düzenlemenin neden yapıldığını açıklayan bir not girin. Bu not, **Fiş düzenlemelerinin denetim izi** sayfasında gösterilir.

   Aynı fişe birden çok düzenleme yapılabilir ve her düzenleme izlenir.

## <a name="audit-trail-of-voucher-edits"></a>Fiş düzenlemelerinin denetim izi

Bu özellik ile yapılan değişiklikleri izlemek için bir denetim kaydı özel olarak tutulur. Fiş düzenlemelerinin denetim kaydına iki şekilde erişebilirsiniz:

  - **Genel muhasebe** > **Sorgular ve raporlar** > **Fiş hareketleri**'ne gidin. **Fiş sorguları** sayfasında, **Fişi düzenle** > **Fiş düzenlemelerinin denetim izi**'ni seçin. Denetim kaydı yalnızca seçilen fiş kaydı için gösterilir. 
   
    Sorguyu bu şekilde açarak, tek bir fiş kaydına yapılan tüm düzenlemelere odaklanabilirsiniz.
  
  - **Genel muhasebe** > **Periyodik görevler** > **Fiş düzenlemelerinin denetim izi**'ne gidin. İletişim kutusunda, düzenlemelerin denetim kayıtlarını görmek istediğiniz fişleri belirtmek için ölçütleri girin. Tüm fişlerin denetim kaydını görüntülemek için, ölçütü boş bırakın ve **Tamam**'ı seçin. 
    
    Sorguyu bu şekilde açarak, belirli bir tarihte veya belirli bir kullanıcı tarafından yapılan düzenlemelere filtre uygulayabilirsiniz.

**Fiş düzenlemelerinin denetim izi** sayfasında aşağıdaki bilgiler gösterilir:

- **Oluşturma tarihi ve saati** – Düzenleme tarihi ve saati.
- **Düzenleme nedeni** – Kullanıcının düzenleme için girdiği neden.
- **Oluşturan** – Düzenlemeyi oluşturan kullanıcı.

Her bir denetim kaydının ayrıntılarını görüntülemek için, **Oluşturma tarihi ve saati** değerini ayrıntılı olarak inceleyin. **Düzenlenen fiş özelliklerini görüntüle** sayfası, önceki açıklama ve güncelleştirilmiş açıklama dahil olmak üzere, orijinal düzenleme sayfasıyla aynı bilgileri gösterir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
