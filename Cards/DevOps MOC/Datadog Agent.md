Datadog Agent là một phần mềm hoạt động trên máy chủ để thu thập và gửi dữ liệu hệ thống về nền tảng Datadog.
- [[Opensource]]
- [Supported Platforms](https://docs.datadoghq.com/agent/supported_platforms)

## Cài đặt Datadog Agent trên Amazon Linux

Phiên bản Agent 7:
> Chạy câu lệnh dưới đây để cài đặt hoặc cập nhật... (Thay thế Datadog apikey của bạn vào phần XXXXXX)
```bash
DD_API_KEY=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX DD_SITE="datadoghq.com" DD_APM_INSTRUMENTATION_ENABLED=host bash -c "$(curl -L https://s3.amazonaws.com/dd-agent/scripts/install_script_agent7.sh)"
```

> Nếu cài đặt phiên bản **Agent <= 7.39** trên hệ điều hành **Amazon Linux 2022** *([[Amazon Linux 2022]] và [[Amazon Linux 2]] là hai phiên bản khác nhau)*, cần phải cài đặt package **libxcrypt-compat**:`dnf install -y libxcrypt-compat`
> Kiểm tra phiên bản của Datadog Agent: `sudo datadog-agent version`
> Kiểm tra phiên bản của hệ điều hành (OS - [[Operating System]]): `uname -a`

Kiểm tra trạng thái của Datadog Agent sau khi cài đặt:
- OS sử dụng [[sysvinit]]: `service datadog-agent status`
- OS sử dụng [[systemd]]: `systemctl status datadog-agent`