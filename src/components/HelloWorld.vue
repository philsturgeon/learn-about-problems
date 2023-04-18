<template>
  <div class="bg-white">
    <div class="relative isolate px-6 pt-14 lg:px-8">
      <div class="mx-auto max-w-2xl py-20">
        <div class="text-center">
          <h1
            class="text-4xl font-bold tracking-tight text-gray-900 sm:text-6xl"
          >
            Get Started with HTTP API Problems
          </h1>
          <p class="mt-6 text-lg leading-8 text-gray-600">
            Everything you need to know about the standard for HTTP API Errors.
          </p>
          <div class="mt-10 flex items-center justify-center gap-x-6">
            <a
              href="#"
              class="rounded-md bg-indigo-600 px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600"
              >Get started</a
            >
            <a href="#" class="text-sm font-semibold leading-6 text-gray-900"
              >Learn more <span aria-hidden="true">→</span></a
            >
          </div>
        </div>
      </div>

      <div class="flex flex-row pb-10">
        <div
          class="basis-1/2 mt-2 text-xl font-bold tracking-tight text-gray-900"
        >
          What is HTTP API Problems?
        </div>
        <div class="basis-1/2">
          HTTP API Problems RFC 7807 is a document that provides a standardized
          way for HTTP APIs to communicate errors or problems to clients. This
          document defines a format for problem details, or error messages, to
          be returned to clients in a consistent and machine-readable way.
        </div>
      </div>

      <div class="flex flex-row pb-10">
        <div
          class="basis-1/2 mt-2 text-xl font-bold tracking-tight text-gray-900"
        >
          When should you use API Problems?
        </div>
        <div class="basis-1/2">
          Having different API errors for different APIs can make it difficult
          for clients to understand how to handle errors and can lead to
          inconsistent error handling across different APIs. Standardizing error
          messages with RFC 7807 can provide consistency and confidence.
        </div>
      </div>

      <div class="flex flex-row pb-10">
        <div
          class="basis-1/2 mt-2 text-xl font-bold tracking-tight text-gray-900"
        >
          How can I add API Problems to my API?
        </div>
        <div class="basis-1/2">
          If you are using a web application framework you can usually find a
          package or component to give you RFC 7807 compliant API error
          messages...
        </div>
      </div>

      <div class="flex flex-row pb-10">
        <div
          class="basis-1/2 mt-2 text-xl font-bold tracking-tight text-gray-900"
        >
          How we use API Problems in Zuplo.
        </div>
        <div class="basis-1/2">Bla bla bla</div>
      </div>

      <!-- <div class="mx-auto grid max-w-2xl grid-cols-1 gap-x-8 gap-y-16 sm:gap-y-20 lg:mx-0 lg:max-w-none lg:grid-cols-2">
        <div class="lg:pr-8 lg:pt-4">
          <div class="lg:max-w-lg">
            <h2 class="text-base font-semibold leading-7 text-indigo-600">Standard errors</h2>
            <p class="mt-2 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">Now more unique snowflakes</p>
            <p class="mt-6 text-lg leading-8 text-gray-600">Every single error message in every API, microservice, API gateway, and every other tool in the chain, and call use the same error format.</p>
            <dl class="mt-10 max-w-xl space-y-8 text-base leading-7 text-gray-600 lg:max-w-none">
              <div v-for="feature in features" :key="feature.name" class="relative pl-9">
                <dt class="inline font-semibold text-gray-900">
                  <component :is="feature.icon" class="absolute left-1 top-1 h-5 w-5 text-indigo-600" aria-hidden="true" />
                  {{ feature.name }}
                </dt>
                {{ ' ' }}
                <dd class="inline">{{ feature.description }}</dd>
              </div>
            </dl>
          </div>
        </div>
        <img src="https://tailwindui.com/img/component-images/dark-project-app-screenshot.png" alt="Product screenshot" class="w-[48rem] max-w-none rounded-xl shadow-xl ring-1 ring-gray-400/10 sm:w-[57rem] md:-ml-4 lg:-ml-0" width="2432" height="1442" />
      </div> -->

      <div class="mx-auto py-20">
        <h1
          class="mb-4 text-3xl font-extrabold leading-none tracking-tight text-gray-900 md:text-4xl lg:text-5xl dark:text-white"
        >
          Error Types
        </h1>
        <p
          class="mb-6 text-lg font-normal text-gray-500 lg:text-xl sm:px-16 xl:px-48 dark:text-gray-400"
        >
          When you're building your API you could build documentation pages
          which explain exactly what every single type of error is, then include
          a link to that page in the JSON error response. You could literally
          have "Ran out of snacks at the office" as an error type. If you don't
          have time for all that, you can use these basic error types based on
          HTTP status codes.
        </p>

        <div
				class="grid grid-flow-row gap-8 text-neutral-600 sm:grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4">
          <div v-for="status in statuses" :key="status.name" class="basis-1/6">
            <a
              href="#"
              class=" block max-w-sm p-6 bg-white border border-gray-200 rounded-lg shadow hover:bg-gray-100 dark:bg-gray-800 dark:border-gray-700 dark:hover:bg-gray-700"
            >
              <h5
                class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white"
              >
                {{ status.code }}: {{ status.name }}
              </h5>

              <p class="font-normal text-gray-700 dark:text-gray-400">
                {{ status.description }}
              </p>
            </a>
           

          </div>
        </div>

      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

import {
  CloudArrowUpIcon,
  LockClosedIcon,
  ServerIcon,
} from "@heroicons/vue/20/solid";

const features = [
  {
    name: "Validation.",
    description:
    "Include validation feedback so clients can automatically build up error messages.",
    icon: CloudArrowUpIcon,
  },
  {
    name: "Custom Variables.",
    description:
    "Add arbitrary extra data to your errors so clients can build custom or i18n errors easily.",
    icon: LockClosedIcon,
  },
  {
    name: "Links to more documentation.",
    description:
      "API clients can have a link to more documentation to learn whats going wrong.",
    icon: ServerIcon,
  },
];


const statuses = [
  {
    code: 100,
    name: 'Continue',
    description: "The server has received the request headers and the client should proceed to send the request body.",
  },
  {
    code: 101,
    name: 'Switching Protocols',
    description: "The server is switching protocols according to the client's request.",
  },
  {
    code: 200,
    name: 'OK',
    description: "The request has succeeded.",
  },
  {
    code: 201,
    name: 'Created',
    description: "The request has been fulfilled and a new resource has been created.",
  },
  {
    code: 202,
    name: 'Accepted',
    description: "The request has been accepted for processing, but the processing has not been completed.",
  },
  {
    code: 203,
    name: 'Non-Authoritative Information',
    description: "The request has been successfully processed, but the returned information may be from a third-party source.",
  },
  {
    code: 204,
    name: 'No Content',
    description: "The request has been successfully processed, but there is no content to return.",
  },
  {
    code: 205,
    name: 'Reset Content',
    description: "The request has been successfully processed, and the client should reset its document view.",
  },
  {
    code: 206,
    name: 'Partial Content',
    description: "The server is delivering only part of the resource due to a range header sent by the client.",
  },
  {
    code: 300,
    name: 'Multiple Choices',
    description: "The requested resource has multiple representations, each with its own location.",
  },
  {
    code: 301,
    name: 'Moved Permanently',
    description: "The requested resource has been permanently moved to a new location.",
  },
  {
    code: 302,
    name: 'Found',
    description: "The requested resource has been temporarily moved to a new location.",
  },
  {
    code: 303,
    name: 'See Other',
    description: "The response to the request can be found under a different URI.",
  },
  {
    code: 304,
    name: 'Not Modified',
    description: "The requested resource has not been modified since the last time it was accessed.",
  },
  {
    code: 307,
    name: 'Temporary Redirect',
    description: "The requested resource has been temporarily moved to a new location, but the client should continue to use the original URI.",
  },
  {
    code: 308,
    name: 'Permanent Redirect',
    description: "The requested resource has been permanently moved to a new location, and future requests should use the new URI.",
  },
  {
    code: 400,
    name: 'Bad Request',
    description: "The request could not be understood or was missing required parameters.",
  },
  {
    code: 401,
    name: 'Unauthorized',
    description: "The authentication credentials are missing or invalid.",
  },
  {
    code: 402,
    name: 'Payment Required',
    description: "This status code is reserved for future use.",
  },
  {
    code: 403,
    name: 'Forbidden',
    description: "The client does not have access rights to the content, i.e., they are unauthorized.",
  },
  {
    code: 404,
    name: 'Not Found',
    description: "The requested resource could not be found.",
  },
  {
    code: 405,
    name: 'Method Not Allowed',
    description: "The request method is not supported for the requested resource.",
  },
  {
    code: 406,
    name: 'Not Acceptable',
    description: "The requested resource is not capable of generating content that is suitable according to the Accept headers sent in the request.",
  },
  {
    code: 407,
    name: 'Proxy Authentication Required',
    description: "The client must first authenticate itself with the proxy.",
  },
  {
    code: 408,
    name: 'Request Timeout',
    description: "The server timed out waiting for the request.",
  },
  {
    code: 409,
    name: 'Conflict',
    description: "The request could not be completed due to a conflict with the current state of the resource.",
  },
  {
    code: 410,
    name: 'Gone',
    description: "The requested resource is no longer available and will not be available again.",
  },
  {
    code: 411,
    name: 'Length Required',
    description: "The request did not specify the length of its content, which is required by the resource.",
  },
  {
    code: 412,
    name: 'Precondition Failed',
    description: "The server does not meet one of the preconditions that the requester put on the request.",
  },
  {
    code: 413,
    name: 'Payload Too Large',
    description: "The request is larger than the server is willing or able to process.",
  },
  {
    code: 414,
    name: 'URI Too Long',
    description: "The URI provided was too long for the server to process.",
  },
  {
    code: 415,
    name: 'Unsupported Media Type',
    description: "The request entity has a media type which the server or resource does not support.",
  },
  {
    code: 416,
    name: 'Range Not Satisfiable',
    description: "The client has asked for a portion of the file, but the server cannot supply that portion.",
  },
  {
    code: 417,
    name: 'Expectation Failed',
    description: "The server cannot meet the requirements of the Expect request-header field.",
  },
  {
    code: 418,
    name: 'I\'m a teapot',
    description: "This status code is a joke, and not meant to be taken seriously.",
  },
  {
    code: 421,
    name: 'Misdirected Request',
    description: "The request was directed at a server that is not able to produce a response.",
  },
  {
    code: 422,
    name: 'Unprocessable Entity',
    description: "The request was well-formed but was unable to be followed due to semantic errors.",
  },
  {
    code: 423,
    name: 'Locked',
    description: "The resource that is being accessed is locked.",
  },
  {
    code: 424,
    name: 'Failed Dependency',
    description: "The request failed due to failure of a previous request.",
  },
  {
    code: 425,
    name: 'Too Early',
    description: "The server is unwilling to risk processing a request that might be replayed.",
  },
  {
    code: 426,
    name: 'Upgrade Required',
    description: "The client should switch to a different protocol such as TLS/1.0, given in the Upgrade header field.",
  },
  {
    code: 428,
    name: 'Precondition Required',
    description: "The origin server requires the request to be conditional.",
  },
  {
    code: 429,
    name: 'Too Many Requests',
    description: "The user has sent too many requests in a given amount of time.",
  },
  {
    code: 431,
    name: 'Request Header Fields Too Large',
    description: "The server is unwilling to process the request because its header fields are too large.",
  },
  {
    code: 451,
    name: 'Unavailable For Legal Reasons',
    description: "The resource is unavailable due to legal reasons.",
  },
  {
    code: 500,
    name: 'Internal Server Error',
    description: "The server encountered an unexpected condition that prevented it from fulfilling the request.",
  },
  {
    code: 501,
    name: 'Not Implemented',
    description: "The server does not support the requested feature.",
  },
  {
    code: 502,
    name: 'Bad Gateway',
    description: "The server received an invalid response from the upstream server while trying to fulfill the request.",
  },
  {
    code: 503,
    name: 'Service Unavailable',
    description: "The server is currently unable to handle the request due to a temporary overload or maintenance of the server.",
  },
  {
    code: 504,
    name: 'Gateway Timeout',
    description: "The server did not receive a timely response from the upstream server while trying to fulfill the request.",
  },
  {
    code: 505,
    name: 'HTTP Version Not Supported',
    description: "The server does not support the HTTP protocol version used in the request.",
  },
  {
    code: 506,
    name: 'Variant Also Negotiates',
    description: "Transparent content negotiation for the request results in a circular reference.",
  },
  {
    code: 507,
    name: 'Insufficient Storage',
    description: "The server is unable to store the representation needed to complete the request.",
  },
  {
    code: 508,
    name: 'Loop Detected',
    description: "The server detected an infinite loop while processing the request.",
  },
  {
    code: 510,
    name: 'Not Extended',
    description: "Further extensions to the request are required for the server to fulfill it.",
  },
  {
    code: 511,
    name: 'Network Authentication Required',
    description: "The client needs to authenticate to gain network access.",
  },
];

// Java : https://github.com/zalando/problem-spring-web

// Node.js : https://www.npmjs.com/package/problem-json

const mobileMenuOpen = ref(false);
</script>
