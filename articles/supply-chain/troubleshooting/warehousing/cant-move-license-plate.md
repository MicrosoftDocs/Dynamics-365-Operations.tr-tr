---
title: Boş çıkışa ve Boş girişe izin verilirse plaka taşınamıyor
description: Seri numarasında Boş çıkışa ve Boş girişe izin veriliyorsa plakayı taşıyamazsınız. Bu, seri numarası alanı isteğe bağlı hale getirilerek düzeltilebilir.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0047f79aa417c8fc910447505f07963d014f54e7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477840"
---
# <a name="cant-move-license-plate-if-serial-number-has-blank-issue-and-blank-receipt-allowed"></a>Seri numarasında Boş çıkışa ve Boş girişe izin veriliyorsa plaka taşınamaz

## <a name="symptoms"></a>Belirtiler

İzleme boyutu grubunda, seri numarasında *Boş çıkışa izin verilir* ve *Boş girişe izin verilir* ayarları varsa ve aynı konumda bazılarında seri numarası olan ve bazılarında olmayan birden fazla plaka varsa **Hareket** menü öğesini kullanarak plakaları taşıyamazsınız.

## <a name="resolution"></a>Çözüm

Bu sorun [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687)'da dağıtılan değişikliklerle düzeltilecektir. Boş girişe ve Boş çıkışa izin verildiğinde bu değişiklikler **Seri numarası** alanını isteğe bağlı yapar.
