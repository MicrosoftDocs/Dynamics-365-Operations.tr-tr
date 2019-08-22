---
title: Belge yazdırma
description: Microsoft Dynamics 365 for Finance and Operations'da belgeleri yerel bir yazıcı veya ağa bağlı bir yazıcı kullanarak yazdırabilirsiniz. Bu makale belgelerin nasıl yazdırılacağına genel bir bakış sağlar.
author: TJVass
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Application User
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bbc45865b55b4794202408ca19a0776440382fdd
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850083"
---
# <a name="document-printing"></a>Belge yazdırma

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations'da belgeleri yerel bir yazıcı veya ağa bağlı bir yazıcı kullanarak yazdırabilirsiniz. Bu makale belgelerin nasıl yazdırılacağına genel bir bakış sağlar.

## <a name="printing-overview"></a>Yazdırmaya genel bakış

Microsoft Dynamics 365 for Finance and Operations iş faaliyetini destekleyen belgeleri oluşturmayı, depolamayı ve dağıtmayı kolay hale getiren tümleşik hizmetler ve istemci uygulamaları sağlar. Finance and Operations'da belgeleri yerel bir yazıcı veya ağa bağlı bir yazıcı kullanarak yazdırabilirsiniz. Ayrıca, Finance and Operations sayfalarını ve raporlarını doğrudan istemciden, PDF dosyası veya Microsoft Office belgeleri olarak dışa aktarabilirsiniz. Son olarak, dağıtılmış iş yükü, ağ kaynaklarını kullanarak doğrudan bir mobil cihazdan işle ilgili belgeleri yazdırmaya olanak sağlar. Yazdırma gereksinimleri farklılık gösterse bile tüm sektörlerin genellikle iş belgelerinin basılı kopyalarını Finance and Operations kullanarak oluşturması gerekir. Barındırılan uygulamalardan ağ cihazlarında belgeleri yazdırmak benzersiz bir sorun kümesi sunar. Burada bazı örnekler verilmiştir:

- Yazıcı sürücüleri kullanıcının cihazında kullanılabilir olmayabilir.
- Kullanıcının cihazı şirket ağına bağlı olmayabilir.

Özel bir ana makine kullanarak ve bazı kolay adımları izleyerek yöneticiler dağıtımları kullanıcıların ağ cihazlarında iş uygulamalarından doğrudan çıktı alabileceği şekilde yapılandırabilir.

### <a name="printing-scenarios-in-finance-and-operations-applications"></a>Finance and Operations uygulamalarında yazdırma senaryoları

Aşağıdaki tabloda Finance and Operations uygulamalarındaki başlıca üç yazdırma senaryosu açıklanır.

| Senaryo                        | Hedef                                                      | Çözüm |
|---------------------------------|-----------------------------------------------------------|----------|
| 1. Gördüğünüzü yazdırma        | Tarayıcıda gösterilmekte olanı yazdırın.             | Tarayıcı için web sayfasının "yazdırmaya uygun" sürümü oluşturulur. |
| 2. Etkileşimli yazdırma         | Hassas bir belgeyi yerel olarak bağlanan cihazdan yazdırın. | Raporun PDF sürümünü dışa aktarabilir ve tarayıcıya indirebilirsiniz. |
| 3. Bir ağ aygıtı üzerinden yazdırma | Hassas bir belgeyi bir etki alanı yazıcı cihazına gönderin.     | Hassas bir belge, müşterinin etki alanında barındırılan sunucu üzerinde çalışan bir istemci uygulamasına gönderilir. |

Çözümler farklılık gösterdiğinden, senaryoya bağlı olarak, Finance and Operations uygulamaları kullanıcıların hedeflerine ulaşmasına yardımcı olan yerleşik hizmetler ve araçlar sunar:

- **Senaryo 1** tarayıcının HTML5 istemcisi işleme işlemi tarafından desteklenir.
- **Senaryo 2** istemci uygulamalarını ve Microsoft Office 365 hizmetlerini kullanır.
- **Senaryo 3** istemci uygulamalarının ve Microsoft Azure içinde barındırılan hizmetlerin desteğini gerektirir.

Azure aboneliğine dağıtılan platformun yanı sıra, Finance and Operations uygulamaları müşterilere etki alanında barındırılan hizmetleri belgeleri yazdırmak üzere daha kolay kullanma konusunda yardımcı olan tümleşik, birinci taraf bir Azure uygulaması sunar.

## <a name="service-overview"></a>Hizmete genel bakış
Barındırılan uygulamalar tarafından üretilen belgeler ağa bağlı cihazda yazdırılmayı beklerken, Azure blob depolamada depolanırlar. [Belge Yönlendirme Aracısı](install-document-routing-agent.md) Azure hizmetleri için güvenli bir kanal oluşturmak üzere Azure kimlik doğrulaması kullanılır.

**Yürütme sırası**

1. Rapor Microsoft SQL Server Reporting Services (SSRS) tarafından oluşturulur ve Azure blob depolamada saklanır. Ekli yazıcı ayarları belgeyle birlikte saklanır.
2. Belge Yönlendirme Aracısı etkin işler için Azure Service Bus kuyruğunu sorgular.
3. Belge, Belge Yönlendirme Aracısı tarafından indirilir ve ağ yazıcısında biriktirilir.

İstemci tabanlı çözüm, müşterilerin yazdırma gereksinimlerinin ölçeğini yönetmesine olanak tanır. Yüksek hacimli yazdırma iş yükleri olan müşteriler eşzamanlı yazdırma işlemlerinin sayısını artırmak için birçok Belge Yönlendirme Aracısı yükleyebilir. Alternatif olarak, bazı müşteriler beklenen yazdırma gereksinimleri için çok az Belge Yönlendirme Aracısı yüklemesine gereksinim duyar.

### <a name="service-components-for-network-printing"></a>Ağdan yazdırma için hizmet bileşenleri

Aşağıdaki şema ağ yazdırma işlemlerini desteklemeye yardımcı olan temel bileşenleri gösterir.

[![service-components-for-network-printing\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)

Tek bir yazıcının birden fazla Belge Yönlendirme Aracısına kaydedilebileceğini unutmayın. Yazıcı tercihlerini çözmek için, barındırılan hizmet her ağ yazıcısını benzersiz şekilde tanımlayan ağ yolunu kullanır. Sonuç olarak, yazıcı birden çok istemci tarafından kaydedildiğinde bile, Finance and Operations uygulamalarında kullanılabilen yazıcılar listesinde tek bir seçim olarak görüntülenir.
