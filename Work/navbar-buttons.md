---
id: 1707905814-QEAK
aliases:
  - navbar buttons
tags: []
---

# navbar buttons
```
            {session && session.user.image &&
              <div className="px-4 gap-2 items-center  sm:flex">
                <Image src={session.user.image} className="rounded-[50%]" width="30" height="30" alt="" />
                <p className="hidden sm:flex">{session.user.name}</p> </div>
            }
            {
              !!session
                ? <Link href="/api/auth/signout">
                  <Button variant={"outline"}>Logout3</Button>
                </Link>

                : <Link href="/api/auth/signin">
                  <Button variant={"outline"}>Login</Button>
                </Link>
            }
```
