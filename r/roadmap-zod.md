#review 

Validação de schema com tipagem estatica [Zod](https://zod.dev/)

ele serve pra criar schemas de tipos
[19:22]
pra validar eles
[19:22]
o exemplo mais simples aqui:
[19:23]
Sem zod:

```js
type User = {
  username: string;
  password: string;
}

function validate(user: User): boolean {
  if (!user.username.matches(/^[a-zA-Z_]+$/)) {
    throw new Error("Username is not valid")
  }

  if (!user.password.matches(/[a-zA-Z]/)) {
    throw new Error("Password doesn't have a letter")
  }

  return true;
}
```

agora com zod dá pra criar um schema pra isso

```js
import { z } from "zod";

const UserSchema = z.object({
  username: z.string().regex(/^[a-zA-Z_]+$/, "Username is not valid!"),
  password: z.string().regex(/[a-zA-Z_]/, "Password doesn't have a letter!")
});

// Vai criar um tipo no estilo { username: string, password: string } usando o schema
type User = z.infer<typeof UserSchema>

function validate(user: User): boolean {
  return UserSchema.safeParse(user).success;
}
```

> [!NOTE]
> só um exemplo besta
> dá pra colocar milhões de regras no schema e ele vai validar tudo pra você, vai te dar as mensagens de erro que não passaram e tal
> dá uma olhada na documentação
