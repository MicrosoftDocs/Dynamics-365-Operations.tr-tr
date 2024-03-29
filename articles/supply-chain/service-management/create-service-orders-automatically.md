---
title: Servis siparişlerini otomatik olarak oluşturma
description: Bir servis sözleşmesi veya birden fazla servis sözleşmesi için servis siparişleri oluşturabilirsiniz.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db9d337166f05f80cfdb9d4b82533117daa871e9
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014734"
---
# <a name="create-service-orders-automatically"></a>Servis siparişlerini otomatik olarak oluşturma    

[!include [banner](../includes/banner.md)]


Bir servis sözleşmesi veya birden fazla servis sözleşmesi için servis siparişleri oluşturabilirsiniz. Oluşturulduklarında, servis siparişlerinizi **Servis siparişleri** formunda görüntüleyebilirsiniz.

Servis siparişleri servis anlaşmasının geçerli periyodu için oluşturulur. **Servis siparişleri oluştur** formunda belirttiğiniz aralık servis sözleşmesinin başlangıç tarihinden önce veya bitiş tarihinden sonraysa, servis siparişleri yalnızca aralığın servis sözleşmesinin süresi içinde yer alan parçası için oluşturulur.

Servis siparişlerini el ile veya servis sözleşmesi satırından otomatik olarak oluşturduğunuzda, satırda bir bitiş tarihi belirlemediyseniz, servis siparişi satırın başlangıç ve bitiş tarihleri tarafından tanımlanan zaman aralığı içinde olmalıdır.

## <a name="create-service-orders-automatically-for-a-service-agreement"></a>Servis anlaşması için otomatik olarak servis siparişleri oluşturma

1.  **Servis yönetimi** \> **Servis sözleşmeleri** \> **Servis sözleşmeleri**'ne tıklayın.

2.  Bir servis anlaşması seçin.

3.  **Teslim et** sekmesine ve ardından **Planlanan servis siparişleri**'ne tıklayın.

4.  Servis dönemini tanımlamak için tarihleri **Başlangıç tarihi** ve **Bitiş tarihi** alanlarında belirtin.

5.  Oluşturulan servis siparişleri listesini göstermek için **Bilgi Günlüğünü Göster** onay kutusunu işaretleyin.

6.  **Hareket türlerini dahil et** alan grubunda hareket türlerini seçin. Hareket türleri, servis anlaşmasında oluşturulan satırları temsil eder ve seçtiğiniz her hareket türü, servis anlaşması satırında belirttiğiniz servis aralığına bağlı olarak çeşitli servis siparişleri oluşturur.

7.  Sürekli bir servis siparişleri serisinde eksik olan servis siparişlerini oluşturmak için **Sürekli** onay kutusunu işaretleyin.

8.  **Tamam** seçeneğini tıklatın.

## <a name="create-service-orders-automatically-for-several-service-agreements"></a>Servis anlaşması için otomatik olarak çeşitli servis siparişleri oluşturma

1.  **Servis yönetimi** \> **Periyodik** \> **Servis siparişleri** \> **Servis siparişleri oluştur**'a tıklayın.

2.  Servis siparişleri oluştururken kullanmak amacıyla ölçüt eklemek veya kaldırmak üzere seçim yapmak **Seç**'e tıklayın.

3.  **Tamam**'a tıklayın.

## <a name="see-also"></a>Ayrıca bkz.

[Servis siparişleri](service-orders.md)

[Servis siparişlerini otomatik oluşturma](auto-create-service-orders.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]