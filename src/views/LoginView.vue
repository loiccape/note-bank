<template>
    <section class="h-screen lg:flex lg:items-center">
        <div class="bg-grey900 h-16 flex justify-center items-center lg:hidden">
            <img src="../assets/images/logo-large.svg" alt="logo finance" />
        </div>

        <div
            class="hidden lg:flex h-full rounded-lg m-4 bg-[url('../assets/images/illustration-authentication.svg')] bg-center bg-cover  p-8 w-1/3  flex-col justify-between">
            <img src="../assets/images/logo-large.svg" alt="logo finance" class="w-20" />

            <div class="text-white w-11/12">
                <p class="text-2xl font-bold">Keep track of your money
                    and save for your future</p>
                <p class="mt-6">
                    Personal finance app puts you in control of your spending. Track transactions, set budgets, and add
                    to savings pots easily.
                </p>
            </div>
        </div>
        <form @submit="onSubmit"
            class="bg-white w-11/12 lg:w-1/3 lg:h-1/2 lg:mx-auto md:w-3/4 mx-auto mt-28 lg:m-0 md:mt-56 p-8 rounded-lg ">
            <FormField v-slot="{ componentField }" name="email">
                <h2 class="text-3xl font-bold mb-6">Login</h2>
                <FormItem class="mb-3">
                    <FormLabel>Email</FormLabel>
                    <FormControl>
                        <Input type="email" v-bind="componentField" />
                    </FormControl>
                    <FormMessage />
                </FormItem>
            </FormField>
            <FormField v-slot="{ componentField }" name="password">
                <FormItem>
                    <FormLabel>Password</FormLabel>
                    <FormControl>
                        <Input type="password" v-bind="componentField" />
                    </FormControl>
                    <FormMessage />
                </FormItem>
            </FormField>
            <Button type="submit" class="w-full mt-10 h-12 text-white bg-grey900">
                Login
            </Button>

            <p class="text-grey500 mt-6 text-center">Need to create an account ? <a href="/"
                    class="font-semibold underline text-grey900">Sign Up</a></p>
        </form>
    </section>
</template>

<script setup lang="ts">

//imports shadcn
import { toTypedSchema } from '@vee-validate/zod'
import * as z from 'zod'
import { useForm } from 'vee-validate'
import {
    FormControl,
    FormField,
    FormItem,
    FormLabel,
    FormMessage
} from '@/components/ui/form'
import { Button } from '@/components/ui/button'
import { Input } from '@/components/ui/input'


const formSchema = toTypedSchema(z.object({
    email: z.string().min(2).max(50).email("The email must be valid"),
    password: z.string()
        .min(7, "Password must be at least 7 characters long")
        .regex(/[A-Z]/, "Password must contain at least one uppercase letter")
        .regex(/[a-zA-Z0-9]/, "Password must be alphanumeric")
}));



const form = useForm({
    validationSchema: formSchema,
})


const onSubmit = form.handleSubmit((values) => {
    console.log('Form submitted!', values)
})
</script>