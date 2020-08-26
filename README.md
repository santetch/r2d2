# FTeam Kata Vamos a crear un proyecto del estilo
# FTeam Kata
Vamos a crear un proyecto del estilo de Steam, pero de minijuegos.

## Iteracion 1
Lo primero que van a hacer nuestros usuarios es poder acceder a su cuenta.
Para ello, deberemos en esta primer iteracion implementar un login funcional.

Por funcional queremos decir:
- Solo los usuarios en [esta lista](#lista-de-usuarios) pueden loggearse 
correctamente.
- Los usuarios pueden usar email o username para acceder.
- Solo existen 2 salidas posibles en el login, acceso permitido o acceso
denegado.

### Lista de usuarios
1) <b>Email</b>: 
tdd@workflow.com
 <b>Username</b>: tdd_workflow <b>Password</b>: aZenWay
2) <b>Email</b>: 
email@domain.com
 <b>Username</b>: beauty_email <b>Password</b>: tellMe2
3) <b>Email</b>: 
elperri@some.com
 <b>Username</b>: perri <b>Password</b>: unaPasswordSeg
4) <b>Email</b>: 
ricardo@fort.com
 <b>Username</b>: rick_fort <b>Password</b>: miameeeeee

## Iteracion 2
Despues de loggearse, el usuario debe ver un menu con 3 opciones disponibles.

Las opciones son:
- [Para los usuarios que ingresan con email](#Usuarios-que-ingresan-con-email)
- [Para los usuarios que ingresan con username](#Usuarios-que-ingresan-con-username)

### Usuarios que ingresan con email
1) <b>Season Games</b>
2) <b>Daily Mission</b>

### Usuarios que ingresan con username
1) <b>Season Games</b>
3) <b>Daily Mission</b>
3) <b>Account</b>

## Iteration 3
Implement a frontend (mobile / web) app.

<b>Constraint</b>: It is not allowed to carry into frontend app the user list.
Must be taken from a remote service that must to be written in this iteration. 
This does not mean that only the users list has to be remote, you can either have your
logic there. The point is to have a backend, divided as you want, with the transport
layer that you want.

## Iteration 4
Implement a sign up. Remove list from iteration 1 and consume the signed up users.

## Iteration 5
Track use cases behaviour into any service that you want. If you do not want to 
really integrate any, at least make a tracker into a log file, with this structure:

```
{
    "event": String,
    "properties": {
        "this_props": "may vary between events",
    }
}
```

As it says, the props are a free json in this example.

The wanted tracks are:
- login.core.Login attempt: must be tracked at beginning of use case, and must track the 
credentials 
- login.core.Login result: must be tracked at finishing the ue case. Must tell if was 
granted or denied
