# DFDE 선박 정리: LNG 운반선의 Dual Fuel Diesel Electric 추진 시스템

> 이 문서는 GitHub `README.md`로 바로 올릴 수 있도록 작성한 DFDE 선박 개념 정리입니다.  
> 대상: LNG선 기관사, 해기사 면접 준비자, 조선/해운 실무 입문자

---

## 1. DFDE란?

**DFDE**는 **Dual Fuel Diesel Electric**의 약자입니다.

즉, **이중연료 엔진(Dual Fuel Engine)**으로 발전기를 돌리고, 그 전기로 **전기 추진 모터**를 구동하여 선박을 움직이는 방식입니다.

간단히 말하면 다음과 같습니다.

```text
LNG Cargo Tank
     ↓
BOG / FBOG
     ↓
Gas Supply System
     ↓
Dual Fuel Generator Engine
     ↓
Main Switchboard
     ↓
Propulsion Transformer / Converter
     ↓
Electric Propulsion Motor
     ↓
Shaft / Propeller
```

DFDE 선박은 주로 **LNG Carrier**에서 사용되었습니다. LNG 화물 탱크에서 자연적으로 발생하는 **BOG(Boil-Off Gas)**를 연료로 활용할 수 있기 때문에 LNG선과 잘 맞는 추진 방식입니다.

---

## 2. 왜 LNG선에서 DFDE가 쓰였나?

LNG는 약 **-163°C**의 극저온 상태로 운반됩니다. 아무리 단열을 잘해도 외부 열이 들어오면 일부 LNG가 기화됩니다. 이렇게 생기는 가스가 **BOG**입니다.

BOG는 그냥 버릴 수 없고, 탱크 압력 관리와 안전을 위해 반드시 처리해야 합니다. DFDE 선박은 이 BOG를 연료로 사용하여 발전하고 추진에 활용합니다.

### 기존 스팀터빈 LNG선과 비교

과거 LNG선은 BOG를 보일러에서 태워 **스팀터빈**을 돌리는 방식이 많았습니다. 하지만 스팀터빈은 구조가 단순하고 신뢰성은 좋지만, 연료 효율이 낮은 편입니다.

DFDE는 스팀터빈보다 효율이 좋고, 운전 부하 변화에 유연하게 대응할 수 있어 한동안 LNG선의 대표적인 추진 방식으로 많이 사용되었습니다.

---

## 3. DFDE의 핵심 구성품

## 3.1 Dual Fuel Generator Engine

DFDE의 중심은 **Dual Fuel 엔진**입니다.

이 엔진은 보통 다음 두 가지 연료를 사용할 수 있습니다.

| 운전 모드 | 주 연료 | 점화 방식 |
|---|---|---|
| Gas Mode | Natural Gas / BOG | 소량의 Pilot Oil로 점화 |
| Diesel Mode | MDO / MGO / HFO 등 | 디젤 압축착화 |

Gas Mode에서는 가스를 주 연료로 쓰지만, 가스는 디젤처럼 압축만으로 쉽게 착화되지 않기 때문에 **Pilot Oil**을 소량 분사해서 점화합니다.

```text
Gas Mode 연소 개념

Air + Gas 혼합기 흡입
        ↓
압축
        ↓
Pilot Oil 소량 분사
        ↓
Pilot Oil 착화
        ↓
Gas-Air Mixture 연소
        ↓
발전기 구동
```

---

## 3.2 Generator

Dual Fuel 엔진은 직접 프로펠러를 돌리지 않고 **발전기**를 돌립니다.

즉, 엔진의 기계적 에너지를 전기에너지로 바꿉니다.

```text
Dual Fuel Engine → Generator → Electric Power
```

이 전기는 추진뿐 아니라 선내 부하에도 사용됩니다.

예를 들면:

- 추진 모터
- Cargo pump
- Ballast pump
- Compressor
- HVAC
- Accommodation load
- Engine room auxiliary machinery

---

## 3.3 Main Switchboard

발전기에서 생산된 전기는 **Main Switchboard**로 모입니다.

Main Switchboard는 선박 전력계통의 중심입니다.

주요 역할은 다음과 같습니다.

- 발전기 병렬 운전
- 전력 분배
- 부하 관리
- 보호 계전
- Blackout 방지
- 추진 전력 공급
- Auxiliary load 공급

DFDE 선박에서는 전력계통 안정성이 매우 중요합니다. 추진도 전기로 하기 때문에 전력계통 문제가 곧 추진력 상실로 이어질 수 있습니다.

---

## 3.4 Propulsion Transformer / Converter

Main Switchboard에서 나온 전기는 바로 추진 모터로 가지 않고, 보통 **Transformer**와 **Converter**를 거칩니다.

역할은 다음과 같습니다.

- 전압 조정
- 주파수 제어
- 모터 속도 제어
- 추진 출력 제어
- 전기적 보호

추진 모터는 선박 속도와 부하에 따라 회전수를 조절해야 하므로 전력변환장치가 필요합니다.

---

## 3.5 Electric Propulsion Motor

DFDE 선박은 전기 추진 방식이므로, 실제 Shaft를 돌리는 것은 **전기 추진 모터**입니다.

```text
Generator Power → Converter → Propulsion Motor → Shaft → Propeller
```

엔진이 직접 Shaft에 연결된 저속 2행정 추진기관과 달리, DFDE는 엔진과 프로펠러 사이가 기계적으로 직접 연결되지 않습니다.

이것이 DFDE의 큰 특징입니다.

---

## 3.6 Gas Supply System

BOG를 엔진 연료로 보내기 위해서는 Gas Supply System이 필요합니다.

주요 구성은 다음과 같습니다.

- LNG Cargo Tank
- BOG line
- LD Compressor / HD Compressor
- Gas Heater
- Gas Valve Unit, GVU
- Gas Master Valve
- Vent / Purge system
- Double wall gas pipe
- Gas detection system
- ESD system

DFDE 엔진은 고압 2행정 ME-GI 엔진처럼 매우 높은 압력의 가스를 요구하지 않는 경우가 많고, 중속 4행정 DF 엔진을 사용하는 경우가 일반적입니다. 그래서 Gas Supply 압력은 시스템 설계에 따라 다르지만, 고압 ME-GI보다 낮은 압력 체계로 구성되는 경우가 많습니다.

---

## 4. DFDE의 운전 모드

## 4.1 Gas Mode

Gas Mode는 BOG 또는 강제기화가스를 주 연료로 사용하는 모드입니다.

특징:

- 연료비 절감 가능
- SOx 배출 거의 없음
- CO2 배출 감소
- Pilot Oil 필요
- Methane slip 발생 가능
- Gas trip 시 Diesel Mode로 전환 필요

Gas Mode에서는 엔진 부하, 가스 압력, 가스 온도, 메탄가, knocking, misfire 등을 지속적으로 감시해야 합니다.

---

## 4.2 Diesel Mode

Diesel Mode는 MDO, MGO, HFO 등의 액체연료로 운전하는 모드입니다.

사용 상황:

- Gas supply 불가
- Gas system 정비
- Port regulation상 gas burning 제한
- Gas trip 발생
- Low load 조건
- BOG 부족
- 엔진 안정성 확보 필요 시

Diesel Mode는 가스 계통에 문제가 있어도 선박 운항을 계속할 수 있게 해주는 백업 역할을 합니다.

---

## 4.3 Fuel Sharing Mode / Mixed Mode

일부 시스템에서는 가스와 액체연료를 일정 비율로 함께 사용하는 운전이 가능합니다.

목적:

- 부하 변동 대응
- 가스 소비량 조절
- BOG 처리 최적화
- 연소 안정성 확보

---

## 5. BOG 처리 개념

LNG선의 핵심은 **탱크 압력 관리**입니다.

BOG가 발생하면 보통 다음 방식으로 처리합니다.

```text
BOG 발생
   ↓
1) DF Engine 연료로 사용
2) GCU에서 소각
3) Reliquefaction Plant로 재액화
4) Forced Vaporizer로 추가 기화
5) Vent, 단 비상 상황에서만 제한적으로 사용
```

### GCU란?

**GCU(Gas Combustion Unit)**는 남는 BOG를 안전하게 태우는 장치입니다.

엔진에서 다 못 쓰는 BOG가 있거나, 엔진이 Gas Mode로 운전하지 못할 때 탱크 압력 상승을 막기 위해 사용됩니다.

---

## 6. DFDE 선박의 장점

## 6.1 연료 유연성

DFDE는 가스와 액체연료를 모두 사용할 수 있습니다.

따라서 항해 조건, 화물 상태, 연료 가격, 항만 규정에 따라 운전 전략을 바꿀 수 있습니다.

---

## 6.2 BOG 활용 가능

LNG선에서는 BOG 처리가 필수입니다. DFDE는 BOG를 추진 연료로 직접 활용할 수 있어 효율적입니다.

---

## 6.3 부하 대응성 우수

발전기 여러 대를 병렬로 운전할 수 있으므로 부하에 따라 엔진 대수를 조절할 수 있습니다.

예를 들어:

```text
저부하 항해: Generator 2대 운전
고부하 항해: Generator 3~4대 운전
입출항: Thruster 부하 고려하여 Generator 추가 투입
Cargo operation: Cargo pump 부하에 맞춰 Generator 운전
```

---

## 6.4 배치 유연성

엔진이 Shaft에 직접 연결되지 않기 때문에 기관실 배치가 비교적 유연합니다.

---

## 6.5 스팀터빈보다 높은 효율

전통적인 스팀터빈 LNG선보다 연료 효율이 좋은 편입니다.

---

## 7. DFDE 선박의 단점

## 7.1 전기 시스템이 복잡함

DFDE는 기계식 추진보다 전기 시스템 의존도가 높습니다.

중요 장비:

- Main switchboard
- Generator breaker
- Protection relay
- Propulsion converter
- Transformer
- Motor cooling system
- PMS, Power Management System
- IAS / AMS

전기 계통 문제가 생기면 추진력에 직접 영향을 줄 수 있습니다.

---

## 7.2 Methane Slip

Gas Mode에서 완전히 연소되지 않은 메탄이 배출될 수 있습니다.

메탄은 온실효과가 강한 가스이기 때문에 환경 규제 측면에서 단점이 될 수 있습니다.

---

## 7.3 유지보수 복잡성

Dual Fuel 엔진, 가스 계통, 전기 추진 계통을 모두 이해해야 합니다.

기관사는 다음 분야를 함께 알아야 합니다.

- Diesel engine
- Gas combustion
- Electrical power system
- Automation
- Gas safety
- Cargo tank pressure control
- ESD logic

---

## 7.4 고장 시 원인 추적이 어려움

DFDE 선박에서 추진 출력 저하가 발생하면 원인이 다양할 수 있습니다.

예를 들면:

```text
Gas pressure low?
Gas valve trip?
Generator load sharing issue?
PMS command issue?
Converter alarm?
Propulsion motor cooling issue?
Engine knocking or misfire?
BOG compressor trip?
MSB breaker trip?
```

그래서 기계, 전기, 자동제어를 함께 보고 판단해야 합니다.

---

## 8. DFDE와 다른 LNG 추진 방식 비교

| 구분 | Steam Turbine | DFDE | ME-GI / X-DF |
|---|---:|---:|---:|
| 주 사용 시기 | 전통 LNG선 | 2000~2010년대 LNG선 | 최신 LNG선 |
| 추진 방식 | 보일러-터빈 | 전기 추진 | 저속 2행정 직접 추진 |
| BOG 활용 | 보일러 연소 | DF 엔진 연료 | DF 저속엔진 연료 |
| 효율 | 낮음 | 중간~높음 | 높음 |
| 구조 | 단순 | 전기계통 복잡 | 고압/저압 가스공급 복잡 |
| 장점 | 신뢰성, 단순함 | 유연성, BOG 활용 | 높은 효율 |
| 단점 | 연비 낮음 | 전기계통 복잡, methane slip | 설비비, 가스공급장치 부담 |

---

## 9. 기관사 관점에서 중요한 포인트

## 9.1 Gas Mode 전환 전 확인사항

Gas Mode로 전환하기 전에는 다음을 확인해야 합니다.

- Gas supply pressure 정상
- Gas temperature 정상
- GVU ready
- Gas detection alarm 없음
- Double wall pipe ventilation 정상
- Pilot oil pressure 정상
- Engine load 조건 만족
- ESD valve 상태 정상
- Inerting / purging sequence 완료
- Control air pressure 정상
- Knock / misfire alarm 없음

---

## 9.2 Watchkeeping 중 주요 감시 항목

```text
Engine Side
- Load sharing
- Exhaust gas temperature deviation
- Cylinder pressure trend
- Knock level
- Misfire alarm
- Pilot oil pressure
- Lube oil pressure / temperature
- Jacket cooling water temperature

Gas Side
- Gas pressure
- Gas temperature
- GVU status
- Gas valve status
- Gas leakage alarm
- Ventilation fan status
- Double wall pipe pressure / flow

Electrical Side
- Generator load
- Busbar voltage
- Frequency
- Power factor
- Breaker status
- Propulsion motor load
- Converter alarm
- PMS command

Cargo Side
- LNG tank pressure
- BOG generation rate
- Compressor status
- GCU status
- Forcing vaporizer status
```

---

## 9.3 Blackout 방지 관점

DFDE 선박은 추진이 전력에 의존하므로 Blackout 방지가 매우 중요합니다.

주의해야 할 상황:

- Thruster 사용 중 발전기 대수 부족
- Cargo pump start 시 순간 부하 증가
- Generator load sharing 불량
- PMS auto start 실패
- Large motor start sequence 오류
- Gas trip 후 Diesel Mode 전환 실패
- Breaker trip
- Busbar fault

---

## 10. 면접에서 설명하는 짧은 답변 예시

### 한국어 답변

DFDE는 Dual Fuel Diesel Electric의 약자로, LNG선에서 많이 사용된 추진 방식입니다. LNG 탱크에서 발생하는 BOG를 Dual Fuel 엔진의 연료로 사용하고, 엔진은 발전기를 돌려 전기를 생산합니다. 이 전기로 추진 모터를 구동하여 프로펠러를 돌립니다. 장점은 BOG를 효율적으로 사용할 수 있고, 발전기 대수를 조절해 부하 대응이 좋다는 점입니다. 반면 전기 추진 계통, 가스 공급 계통, 자동제어 계통이 복잡해서 기관사는 엔진뿐 아니라 전기와 가스 안전 시스템까지 이해해야 합니다.

### 영어 답변

DFDE stands for Dual Fuel Diesel Electric. It is a propulsion system commonly used on LNG carriers. Boil-off gas from the LNG cargo tanks can be used as fuel for dual-fuel generator engines. These engines drive generators, and the generated electricity is supplied to propulsion motors through the main switchboard and converters. The main advantages are fuel flexibility, efficient use of boil-off gas, and good load management. However, the system is more complex because engineers need to understand dual-fuel engines, gas supply systems, electric propulsion, power management, and safety systems.

---

## 11. 핵심 요약

DFDE 선박을 한 문장으로 정리하면 다음과 같습니다.

> **BOG와 액체연료를 모두 사용할 수 있는 Dual Fuel 엔진으로 전기를 만들고, 그 전기로 추진 모터를 돌리는 LNG선 추진 시스템이다.**

가장 중요한 키워드는 다음과 같습니다.

- DFDE = Dual Fuel Diesel Electric
- BOG = Boil-Off Gas
- Dual Fuel Generator Engine
- Gas Mode / Diesel Mode
- Main Switchboard
- Propulsion Motor
- PMS, Power Management System
- GVU, Gas Valve Unit
- GCU, Gas Combustion Unit
- Tank pressure control
- Gas safety and ESD

---

## 12. 참고 자료

- Wärtsilä, dual-fuel engine and LNG carrier DF engine materials
- ABS / class guidance materials on LNG carrier propulsion and gas-fuelled systems
- IMO MARPOL Annex VI and IMO 2020 sulphur regulation background
- General LNG carrier technical literature on BOG handling and DFDE propulsion

