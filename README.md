# Django Messages DRF

[![CircleCi](https://img.shields.io/circleci/project/github/tarsil/django-messages-drf.svg)](https://circleci.com/gh/tarsil/django-messages-drf)
[![codecov](https://codecov.io/gh/tarsil/django-messages-drf/branch/master/graph/badge.svg?token=VfTlWQlGeF)](https://codecov.io/gh/tarsil/django-messages-drf)

__Official Documentation__ - https://tarsil.github.io/django-messages-drf/

---

## Table of Contents

- [About Django Messages DRF](#about-django-messages-drf)
  - [Overview](#overview)
  - [Versions](#supported-django-and-python-versions)
- [Documentation](#documentation)
  - [Installation](#installation)
  - [Reference Guide](#reference-guide)
    - [Matrix](#url–view–template-matrix)
- [CHANGELOG](docs/release-notes.md)
- [Documentation and Support](#documentation-and-support)
- [License](#license)

---

## About Django Messages DRF

Django Messages DRF is an alternative and based on pinax-messages but using
Django Rest Framework by making it easier to integrate with your existing project.

A special thanks to pinax for inspiring me to do this and use some ideas.

### Overview

`django-messages-drf` is an app for providing private user-to-user threaded
messaging.

#### Supported Django and Python Versions

| Django / Python | 3.6 | 3.7 | 3.8 | 3.9
| --------------- | --- | --- | --- | ---
| 2.2  | Yes | Yes | Yes | Yes |
| 3.0  | Yes | Yes | Yes | Yes |
| 3.1  | Yes | Yes | Yes | Yes |
| 3.2  | Yes | Yes | Yes | Yes |

## Documentation

### Installation

To install django-messages:

```shell
$ pip install django-messages-drf
```

Add `django_messages_drf` to your `INSTALLED_APPS`:

```python
INSTALLED_APPS = [
    # other apps
    "django_messages_drf",
]
```

Run Django migrations to create `django-messages-drf` database tables:

```shell
$ python manage.py migrate
```

Add `django_messages_drf.urls` to your project urlpatterns:

```python
    urlpatterns = [
        # other urls
        url(r"^messages-drf/", include("django_messages_drf.urls", namespace="django_messages_drf")),
    ]
```

### Reference Guide

#### URL–View–Template Matrix

| URL Name  | View   |
| :-------- | :----- |
| `django_messages_drf:inbox`               | `InboxListApiView` |
| `django_messages_drf:thread`      | `ThreadListApiView` |
| `django_messages_drf:thread-create` | `ThreadCRUDApiView` |
| `django_messages_drf:thread-send`       | `ThreadCRUDApiView` |
| `django_messages_drf:thread-delete`       | `ThreadCRUDApiView` |
| `django_messages_drf:message-edit`       | `EditMessageApiView` |

## Documentation and Support

Full documentation for the project is available at https://tarsil.github.io/django-messages-drf/

## License

Copyright (c) 2020-present Tiago Silva and contributors under the [MIT license](https://opensource.org/licenses/MIT).
