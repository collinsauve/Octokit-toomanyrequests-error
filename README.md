# Octokit-toomanyrequests-error

Reproducing what looks like a bug in Octokit

To reproduce:

```bash
bundle install
pry
```

Within pry:

```
require 'octokit'
raise Octokit::TooManyRequests
```

Should raise this error:

> NameError: uninitialized constant Octokit::RateLimit
>
>          @context = Octokit::RateLimit.from_response(@response)
>                            ^^^^^^^^^^^
> from ~/.rbenv/versions/3.1.2/lib/ruby/gems/3.1.0/gems/octokit-4.23.0/lib/octokit/error.rb:39:in `build_error_context'
