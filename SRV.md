## Services

### Діагностичні команди для перевірки послуги @prof.ukrtel.net

#### Пошук irb абонента
    show route [ip_address] | match irb
Має видати результат без приставки "to", в такому випадку, якщо видає "to" - то абонент термінується не на цьому РЕ

#### Перегляд конфігурації абонента (unit)
    show configuration | display set | match [цифри з попередньої команди]

#### Перегляд мак-адреси від абонента
    show bridge mac-table interface ae0.[знову вставляємо цифри з команди пошуку irb]
####
    show arp | match [цифри з irb]

#### ping послуги Prof-internet
    ping [ip_address]

#### Переглянути трафік від абонента
    monitor interface ae0.[цифри з irb абонента]


### Діагностичні команди для перевірки послуги @ethernet.vrf
#### Пошук irb абонента
    show route table l3vpn-[vrf-абонента] [ip_address] | match irb
Має видати результат без приставки "to", в такому випадку, якщо видає "to" - то абонент термінується не на цьому РЕ

#### Перегляд конфігурації абонента (unit)
    show configuration | display set | match [цифри з попередньої команди]

#### Перегляд мак-адреси від абонента
    show bridge mac-table interface ae0.[знову вставляємо цифри з команди пошуку irb]
####
    show arp | match [цифри з irb]

### ping послуги L3VPN
    ping routing-instance l3vpn-[vrf] [ip_address]

#### Переглянути трафік від абонента
    monitor interface ae0.[цифри з irb абонента]

### Сесійні послуги (@gpon.ukrtel.net, @fttb.ukrtel.net, @dsl.ukrtel.net)
#### Перегляд інформації по сесії абонента
Дивитися в УС, на якому РЕ встановлена сесія абонента (L/R)

#### Перегляд сесії на РЕ
    show dhcp relay binding [ip_address]

#### Пінг абонента
    ping [ip_address]

#### Перегляд наявності трафіку від абонента
	  show subscribers | match [ip_address]
Нам поверне результат demux.123456, копіюємо його
####
	  monitor interface [demux.123456]
