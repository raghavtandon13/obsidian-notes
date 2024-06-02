---
id: 1707975929-next-hirrin-signin-page
aliases:
  - next hirrin signin page
tags: []
---

# next hirrin signin page

```
/* eslint-disable react-hooks/rules-of-hooks */
"use client";
import { Button } from "@/components/ui/button";
import React from "react";
import { useForm, SubmitHandler } from "react-hook-form";

type Inputs = {
  email: string;
  password: string;
};

const page = () => {
  const {
    register,
    handleSubmit,
    formState: { errors, isLoading },
  } = useForm<Inputs>();

  const onSubmit: SubmitHandler<Inputs> = async (data: any) => {
    console.log("check this:",data.json());
    // const yoyo = await fetch("/api/auth", { method: "POST", body: JSON.stringify(data) });
  };

  return (
    <div className="flex h-screen items-center justify-center border-gray-800 pt-[70px]">
      <div className="flex flex-col items-stretch justify-center gap-4 sm:flex-row">
        <div className="flex h-full w-max flex-col items-start justify-center p-10">
          <h1 className="text-[32px]">Your Future Awaits</h1>
          <h1 className="text-[32px]">Lets Dive In! </h1>
        </div>
        <div className="rounded-md border-gray-300 bg-gray-100 ">
          <div className="flex w-full flex-col items-center justify-center gap-4 px-10 pb-4 pt-10"></div>
          <form onSubmit={handleSubmit(onSubmit)} className="flex flex-col  items-center justify-center gap-4 rounded-md p-10 pt-0">
            <h1 className="text-2xl font-medium">Login</h1>
            <input
              {...register("email", {
                required: "required baby",
                minLength: { value: 10, message: "enter 10 baby" },
                validate: (value) => {
                  if (!value.includes("@")) {
                    return "should have an @";
                  }
                  return true;
                },
              })}
              className="rounded-md border border-gray-300 p-2"
              type="text"
              placeholder="Email"
            />
            {errors.email && <p className="text-red-500">{errors.email.message}</p>}
            <input
              {...register("password", { required: true, minLength: 8 })}
              className="rounded-md border border-gray-300 p-2"
              type="password"
              placeholder="Password"
            />
            <Button variant={"outline"} type="submit">
              {isLoading ? "Loading" : "Login"}
            </Button>
          </form>
        </div>
      </div>
    </div>
  );
};

export default page;

```
