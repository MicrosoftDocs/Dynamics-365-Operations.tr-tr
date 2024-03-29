---
title: Belge yazdırmaya genel bakış
description: Belgeleri yerel bir yazıcı veya ağa bağlı bir yazıcı kullanarak yazdırabilirsiniz. Bu makale belgelerin nasıl yazdırılacağına genel bir bakış sağlar.
author: RichdiMSFT
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: IT Pro, Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 69161,  ""intro-internal
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.openlocfilehash: 840a635af14e5140834e5c1d2b319d0c8c4bff14
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280879"
---
# <a name="document-printing-overview"></a>Belge yazdırmaya genel bakış

[!include [banner](../includes/banner.md)]

Belgeleri yerel bir yazıcı veya ağa bağlı bir yazıcı kullanarak yazdırabilirsiniz. Bu makale belgelerin nasıl yazdırılacağına genel bir bakış sağlar.

## <a name="printing-overview"></a>Yazdırmaya genel bakış

Uygulama, iş faaliyetini destekleyen belgeleri oluşturmayı, depolamayı ve dağıtmayı kolaylaştıran tümleşik hizmetleri ve istemci uygulamalarını sağlar. Belgeleri yerel bir yazıcı veya ağa bağlı bir yazıcı kullanarak yazdırabilirsiniz. Ayrıca, sayfa ve raporları doğrudan istemciden PDF dosyası veya Microsoft Office belgeleri olarak dışarı aktarabilirsiniz. Son olarak, dağıtılmış iş yükü, ağ kaynaklarını kullanarak doğrudan bir mobil cihazdan işle ilgili belgeleri yazdırmaya olanak sağlar. Yazdırma gereksinimleri farklılık gösterse bile tüm sektörler, genellikle uygulamayı kullanarak iş belgelerinin basılı kopyalarını oluşturmalıdır. Barındırılan uygulamalardan ağ cihazlarında belgeleri yazdırmak benzersiz bir sorun kümesi sunar. Burada bazı örnekler verilmiştir:

- Yazıcı sürücüleri kullanıcının cihazında kullanılabilir olmayabilir.
- Kullanıcının cihazı şirket ağına bağlı olmayabilir.

Özel bir ana makine kullanarak ve bazı kolay adımları izleyerek yöneticiler dağıtımları kullanıcıların ağ cihazlarında iş uygulamalarından doğrudan çıktı alabileceği şekilde yapılandırabilir.

### <a name="application-printing-scenarios"></a>Uygulama yazdırma senaryoları 

Aşağıdaki tabloda üç birincil yazdırma senaryosu açıklanmaktadır.

| Senaryo                        | Hedef                                                      | Çözüm |
|---------------------------------|-----------------------------------------------------------|----------|
| 1. Gördüğünüzü yazdırma        | Tarayıcıda gösterilmekte olanı yazdırın.             | Tarayıcı için web sayfasının "yazdırmaya uygun" sürümü oluşturulur. |
| 2. Etkileşimli yazdırma         | Hassas bir belgeyi yerel olarak bağlanan cihazdan yazdırın. | Raporun PDF sürümünü dışa aktarabilir ve tarayıcıya indirebilirsiniz. |
| 3. Bir ağ aygıtı üzerinden yazdırma | Hassas bir belgeyi bir etki alanı yazıcı cihazına gönderin.     | Hassas bir belge, müşterinin etki alanında barındırılan sunucu üzerinde çalışan bir istemci uygulamasına gönderilir. |

Çözümler farklılık gösterdiğinden, senaryoya bağlı olarak uygulamalar, kullanıcıların hedeflerine ulaşmasına yardımcı olan yerleşik hizmet ve araçlar sunar:

- **Senaryo 1** tarayıcının HTML5 istemcisi işleme işlemi tarafından desteklenir.
- **Senaryo 2** istemci uygulamalarını ve Microsoft 365 hizmetlerini kullanır.
- **Senaryo 3** istemci uygulamalarının ve Microsoft Azure içinde barındırılan hizmetlerin desteğini gerektirir.

Azure aboneliğine dağıtılan platformun yanı sıra, finans ve operasyon uygulamaları müşterilere etki alanında barındırılan hizmetleri belgeleri yazdırmak üzere daha kolay kullanma konusunda yardımcı olan tümleşik, birinci taraf bir Azure uygulaması sunar.

## <a name="service-overview"></a>Hizmete genel bakış
Barındırılan uygulamalar tarafından üretilen belgeler ağa bağlı cihazda yazdırılmayı beklerken, Azure blob depolamada depolanırlar. [Ağdan yazdırmayı etkinleştirmek için Belge Yönlendirme Aracısı'nı yükleme](install-document-routing-agent.md) Azure hizmetleri için güvenli bir kanal oluşturmak üzere Azure kimlik doğrulaması kullanılır.

**Yürütme sırası**

1. Rapor Microsoft SQL Server Reporting Services (SSRS) tarafından oluşturulur ve Azure blob depolamada saklanır. Ekli yazıcı ayarları belgeyle birlikte saklanır.
2. Belge Yönlendirme Aracısı etkin işler için Azure Service Bus kuyruğunu sorgular.
3. Belge, Belge Yönlendirme Aracısı tarafından indirilir ve ağ yazıcısında biriktirilir.

İstemci tabanlı çözüm, müşterilerin yazdırma gereksinimlerinin ölçeğini yönetmesine olanak tanır. Yüksek hacimli yazdırma iş yükleri olan müşteriler eşzamanlı yazdırma işlemlerinin sayısını artırmak için birçok Belge Yönlendirme Aracısı yükleyebilir. Alternatif olarak, bazı müşteriler beklenen yazdırma gereksinimleri için çok az Belge Yönlendirme Aracısı yüklemesine gereksinim duyar.

### <a name="service-components-for-network-printing"></a>Ağdan yazdırma için hizmet bileşenleri

Aşağıdaki şema ağ yazdırma işlemlerini desteklemeye yardımcı olan temel bileşenleri gösterir.

[![service-components-for-network-printing\_2016.](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)

Tek bir yazıcının birden fazla Belge Yönlendirme Aracısına kaydedilebileceğini unutmayın. Yazıcı tercihlerini çözmek için, barındırılan hizmet her ağ yazıcısını benzersiz şekilde tanımlayan ağ yolunu kullanır. Sonuç olarak, yazıcı birden çok istemci tarafından kaydedildiğinde bile uygulamalarda kullanılabilen yazıcılar listesinde tek bir seçim olarak görüntülenir.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
