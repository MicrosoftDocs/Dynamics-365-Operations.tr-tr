---
title: Servis aralıkları
description: Bu konuda, servis aralıklarıyla nasıl çalışılacağına ilişkin bir genel bakış sağlanmaktadır. Servis sözleşmesi aralığı, servis siparişlerini otomatik olarak oluşturduğunuzda servis siparişi satırlarının oluşturulma sıklığını gösterir.
author: kamaybac
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 08ec58037657f7d04e50c31aec0f343a09b9fa4e
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580324"
---
# <a name="service-intervals"></a>Servis aralıkları

[!include [banner](../includes/banner.md)]

Servis sözleşmesi aralığı, servis siparişlerini otomatik olarak oluşturduğunuzda servis siparişi satırlarının oluşturulma sıklığını gösterir.

Servis siparişlerini otomatik olarak oluşturduğunuzda servis siparişi satırları, sözleşme satırının başlangıç tarihinden başlayarak, servis sözleşmesi satırı için belirlediğiniz aralığa göre oluşturulur.

**Servis sözleşmeleri** sayfasındaki servis sözleşmesi satırının **Aralık** alanı boşsa satır bir defalık bir olaydır ve bu servis siparişlerini yinelenen şekilde oluşturmak için kullanılmaz.

## <a name="example"></a>Örnek

Bu örnek, bir servis aralığının bir servis siparişinde servis sözleşmesi satırlarını ve servis siparişi satırlarını nasıl etkileyeceğini gösterir.

### <a name="create-a-service-agreement"></a>Servis sözleşmesi oluşturma

Servis sözleşmesi oluştururken ilk olarak **Servis siparişlerini birleştir** seçeneğini, **Servis sözleşmesine göre** olarak ayarlayın.

1. **Servis sözleşmeleri**'ne tıklayın.
2. Yeni bir servis sözleşmesi oluşturmak için **Eylem Bölmesi**'nde **Servis sözleşmesi** sekmesinde, **Yeni** grubundaki **Servis sözleşmesi**'ne tıklayın.
3. Açıklama girin, **Proje Kodu** alanında bir proje seçin ve **Başlangıç Tarihi** alanına tarih girin.
4. **Servis siparişlerini birleştir** alanında, **Servis sözleşmesine göre**'yi seçin.

Artık aşağıdaki servis sözleşmesini oluşturmuş bulunuyorsunuz:

| Proje      | Başlangıç tarihi                                                                         |
|--------------|------------------------------------------------------------------------------------|
| Projeniz | Proje için belirlediğiniz tarih. Bu örnekte, güncel tarih kullanılır. |

### <a name="create-a-service-agreement-line"></a>Servis sözleşmesi satırı oluşturma

Ardından, **Saat** hareket türüne sahip bir servis sözleşmesi satırı oluşturursunuz.

Örneğin bu bölümünü tamamlamak için **Servis aralıkları** sayfasında 10 günlük bir servis aralığı oluşturmanız gerekir. 

1. Yeni oluşturduğunuz servis sözleşmesini seçin. 
2. **Servis sözleşmeleri** sayfasının alt bölmesinde yeni bir satır oluşturmak için **Satırlar** hızlı sekmesinde **Ekle** düğmesine tıklayın.
3. **Hareket türü** alanında **Saat**'i seçin.
4. **Çalışan** alanında servisi verecek çalışanı seçin.
5. **Servis aralığı** alanında, 10 günlük aralığı seçin.

Şimdi aşağıdaki bilgileri içeren bir servis sözleşmesi satırı oluşturdunuz:

| Hareket türü | Başlangıç tarihi                               | Servis aralığı |
|------------------|------------------------------------------|------------------|
| Saat             | Güncel tarih.                        | 10 günde bir    |
| Çalışan           | Servisi gerçekleştirecek çalışan. |                  |

Satır için belirtilen zaman aralığı yok. 

### <a name="create-planned-service-orders"></a>Planlanan servis siparişleri oluşturma

Şimdi gelecek aya ait planlanan servis siparişleri ve servis siparişi satırları oluşturabilirsiniz.

1. **Servis sözleşmeleri** sayfasında, **Eylem Bölmesi**'nde, **Teslim Et** sekmesindeki **Planlanan servis siparişleri**'ne tıklayın.
2. **Servis siparişleri oluştur** sayfasında, **Başlangıç Tarihi** alanında güncel tarihi ve **Bitiş Tarihi** alanında güncel tarihten bir ay sonraki tarihi girin.
3. **Saat** kaydırıcısını **Evet** konumuna getirin. 
4. **Tamam** seçeneğini tıklatın.

Servis siparişinde hiçbir gruplandırma bulunmadığından ( **Servis siparişlerini birleştir** alanındaki **Servis sözleşmesine göre** seçeneğiyle tanımlanır), servis siparişi başına bir servis siparişi satırı oluşturulur.

### <a name="service-orders-created"></a>Oluşturulan servis siparişleri

Üç servis siparişi satırı, **Servis siparişleri oluştur** iletişim kutusunda belirttiğiniz zaman çerçevesinin sınırları içinde oluşturulmuştur. Servis siparişi satırlarını **Servis sözleşmeleri** sayfasında (**Eylem Bölmesi** \> **Teslim Et** sekmesi \>**Görüntüle** düğmesi) görüntüleyebilirsiniz.

## <a name="related-topics"></a>İlgili konular

[Servis aralıkları ayarlama](set-up-service-intervals.md)  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]