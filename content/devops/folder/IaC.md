---
title: Infrastructure as Code (IaC) – Infrastruktura jako kod
type: devops
#prev: devops/folder/
#next: devops/folder/leaf
sidebar:
  open: true
---

**Infrastructure as Code (IaC)** to praktyka zarządzania infrastrukturą IT przy użyciu kodu zamiast ręcznej konfiguracji. Dzięki IaC serwery, sieci i inne zasoby mogą być definiowane, wersjonowane i wdrażane w sposób powtarzalny i automatyczny.

**1. Dlaczego Infrastructure as Code?**
   
✅ Korzyści z IaC:

- Automatyzacja – eliminacja ręcznej konfiguracji serwerów
- Powtarzalność – środowiska testowe i produkcyjne są identyczne
- Szybkość wdrażania – uruchomienie całej infrastruktury w minutach
- Eliminacja błędów – redukcja ludzkich pomyłek
- Łatwość wersjonowania – infrastruktura zarządzana jak kod aplikacji (Git, CI/CD)

**2. Jak działa IaC?**

IaC pozwala zdefiniować infrastrukturę w plikach konfiguracyjnych, które następnie są przetwarzane przez narzędzia automatyzujące jej tworzenie i zarządzanie. Istnieją dwa podejścia do IaC:
Deklaratywne (np. Terraform, CloudFormation)

    Określasz stan końcowy, a narzędzie samo decyduje, jak go osiągnąć.
    Przykład:

    resource "aws_instance" "web" {
      ami           = "ami-123456"
      instance_type = "t2.micro"
    }

    Zalety: łatwiejsze utrzymanie, lepsza kontrola nad zmianami

Imperatywne (np. Ansible, Chef, Puppet)

    Opisujesz krok po kroku, jak ma wyglądać konfiguracja.
    Przykład (Ansible – YAML):

    - name: Instalacja serwera Nginx
      hosts: web_servers
      tasks:
        - name: Zainstaluj Nginx
          apt:
            name: nginx
            state: present

    Zalety: większa elastyczność w dostosowywaniu konfiguracji

**3. Popularne narzędzia IaC**

| Narzędzie       | Typ           | Zastosowanie                                   |
|----------------|--------------|----------------------------------------------|
| **Terraform**   | Deklaratywne  | Tworzenie infrastruktury w chmurze (AWS, GCP, Azure) |
| **Ansible**     | Imperatywne   | Automatyzacja konfiguracji serwerów          |
| **CloudFormation** | Deklaratywne  | Infrastruktura jako kod w AWS               |
| **Puppet**      | Imperatywne   | Zarządzanie konfiguracją na dużą skalę       |
| **Chef**        | Imperatywne   | Automatyzacja zarządzania serwerami         |

**4. IaC w praktyce – Jak wygląda proces?**

1️⃣ Definiujesz infrastrukturę w pliku kodu (np. Terraform, YAML)
2️⃣ Wersjonujesz kod w systemie kontroli wersji (np. Git)
3️⃣ Testujesz konfigurację na środowisku testowym
4️⃣ Automatycznie wdrażasz w chmurze lub na serwerach
5️⃣ Monitorujesz i aktualizujesz konfigurację w razie potrzeby

**5. Podsumowanie**

IaC to kluczowy element DevOps, pozwalający na szybkie, powtarzalne i bezpieczne zarządzanie infrastrukturą IT. Dzięki IaC firmy mogą szybciej wdrażać aplikacje, minimalizować błędy i lepiej skalować zasoby.