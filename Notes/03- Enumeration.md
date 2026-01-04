
## SMB

اول جزء عن طريق ال NULL Session

```
rpcclient -U "" -N 192.168.222.137
 enumdomusers >> هتطلع اليوزر تحفظهم عندك
 queryuser 0x3e8 >> هتحط ال rid بتاع اليوزر عشان تعرف شويه معلومات
  
```

تاني حاجه عن طريق Session with username and password

```
rpcclient -U "test" 192.168.222.137
```

تالت حاجه عن طريق تول اتوماتيك Enum4Linux

```
enum4linux 192.168.222.137 
```

## SMTP

```
smtp-user-enum -M VRFY -U users.txt -t 192.168.222.137
```

## LDAP

عشان نعرف اسم الدومين 

```
ldapsearch -H ldap://192.168.222.133 -x -s base namingcontexts
```

وبعدين خد الدومين ده طلع منه كل حاجه

```
ldapsearch -H ldap://192.168.222.133 -x -b "DC=nti,DC=local" "objectclass=*"
```

لو الامر اللي فوق ظهرلك ايرور جرب الامر ده حط اليوزر نيم وبالساورد

```
ldapsearch -H ldap://192.168.222.133 -x -D "NTI\\Administrator" -W -b "DC=nti,DC=local"
```


## DNS Zone Transfer

```
dig +noall +answer microsoft.com NS
dig +noall +answer @ns1.msft.net microsoft.com AXFR
dig +noall +answer @ns2.msft.net microsoft.com AXFR
dig +noall +answer @ns3.msft.net microsoft.com AXFR
dig +noall +answer @ns4.msft.net microsoft.com AXFR
dig +noall +answer zonetransfer.me NS
dig +noall +answer @nsztm1.digi.ninja zonetransfer.me AXFR
dig +noall +answer @nsztm2.digi.ninja zonetransfer.me AXFR
dnsrecon -d microsoft.com -t axfr
dnsrecon -d zonetransfer.me -t axfr
```
